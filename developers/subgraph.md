# 🛰 Subgraph

All on-chain data and events from HyperVIBES are indexed via TheGraph.

You can build HyperVIBES-based applications without ever having to deploy a smart contract by creating a realm and building a web3 dapp frontend.

A unique subgraph is deployed for each blockchain network HyperVIBES is on.

{% content-ref url="links-and-repos.md" %}
[links-and-repos.md](links-and-repos.md)
{% endcontent-ref %}

### Examples Queries

Like all GraphQL APIs, you can use introspection to explore the schema, types, and queries available in the subgraph. Below are a few possible ways of using the subgraph:

#### List all realms

```graphql
{
  realms(orderBy: createdAtTimestamp, orderDirection: desc) {
    id
    name
    description
    token
    createdAtTimestamp
  }
}
```

#### Get infusion info for an NFT across all realms

```graphql
{
  nfts(where: { 
    collection: "0xc0877d217b1b83a3347c1703032ae1e013a8fd9f" 
    tokenId: "11" 
  }) {
    tokenId
    collection { address }
    owner { address }

    # there will be 1 Infusion entity for-each Realm this NFT is infused in
    infusions {
      realm { id name }
      balance
      lastClaimAtTimestamp

      # all discrete infusion and claim events will be here
      events {
        eventType
        amount
        msgSender { address }
        target { address }
        createdAtTimestamp
      }
    }
  }
}
```

#### Get details and infused NFTs for a specific realm

```graphql
{
  realm(id: "3") {
    id
    name
    description
    token
    createdAtBlock
    createdAtTimestamp
    dailyRate

    # constraints

    minInfusionAmount
    maxInfusionAmount
    maxTokenBalance
    allowMultiInfuse
    allowPublicInfusion
    allowAllCollections
    requireNftIsOwned

    # configuration

    realmAdmins { account { address } }
    realmInfusers { account { address } }
    realmCollections { collection { address } }

    # get all infused nfts, balances, info, and events (claims and infusions)

    infusions {
      balance
      lastClaimAtTimestamp
      nft { tokenId collection { address } owner { address } }
      events {
        createdAtTimestamp
        target { address }
        amount
        eventType
      }
    }
  }
}
```

#### Get details about a specific account (wallet / agent)

```
{
  account(id:"0xa34c3476ae0c4863fc39e32c0e666219503bed9f") {
    address

    # realms this account is admin for
    realmAdmins { realm { id name } }

    # realms this account is an infuser for
    realmInfusers { realm { id name } }

    # realms this account has created
    createdRealms {id name}

    # any accounts this account can infuse on behalf of
    infusionProxiesAsProxy { realm { id name } infuser { address } }

    # any accounts that can infuse on behalf of this account
    infusionProxiesAsInfuser { realm { id name } proxy { address } }

    # all nfts owned by this account that have been infused across all realms
    ownedNFTs {
      tokenId
      collection { address }
      infusions { realm { id name } balance }
    }

    # find all discrete infusions this account has executed
    infusionEventsAsTarget(where:{ eventType: INFUSE }) {
      amount
      infusion {
        realm { id name }
        nft { tokenId collection {address} owner { address } }
      }
    }
  }
}
```
