# 🏗 Integration

HyperVIBES can be used entirely from the UI without having to write any code.

Deeper integration and customization is possible for developers and builders who wish to deploy their own smart contracts.

{% hint style="info" %}
**Thinking of building an advanced integration with HyperVIBES? **

Come hang in the [**Rarible DAO Discord**](https://discord.gg/ZtZqH7nfgG), we'd love to hear what you have in mind and would be happy to answer any questions .
{% endhint %}

{% content-ref url="../use-cases.md" %}
[use-cases.md](../use-cases.md)
{% endcontent-ref %}

### Client-side Integration&#x20;

If you are wanting to display HyperVIBES data in your own web app such as:

* Infused token balances for a given NFT in a specific realm
* All NFTs infused within a specific realm
* All realms an NFT has been infused within
* All infused NFTs owned by a specific address
* All addresses that have infused a specific NFT
* All NFTs infused by a specific address
* All token claims executed by a specific address

The deployed subgraphs index all data and events from HyperVIBES, which can be queried client-side via GraphQL HTTP requests:

{% content-ref url="subgraph.md" %}
[subgraph.md](subgraph.md)
{% endcontent-ref %}

### Smart Contract Integration

Smart contracts can directly integrate the HyperVIBES protocols to implement the following extensions:

* **Custom infusion logic or constraints**, such infusion-by-vote, reputation-based infusion access, shared infusion token pools, etc
* **Infuse-on-mint functionality**. Create a custom ERC-721 contract that will automatically create a realm on deployment and infuse all minted tokens in the same transaction they are created.
* **Custom claim functionality**, such as taking a fee during executed claims, splitting claims to several addresses, sophisticated and dynamic role-based claiming

{% content-ref url="links-and-repos.md" %}
[links-and-repos.md](links-and-repos.md)
{% endcontent-ref %}
