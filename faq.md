# ❓ FAQ

### What is provenance mining?

Provenance mining is a mechanism that allows an NFT to mine tokens over time which the owner of the NFT can claim. Unclaimed tokens stay within the NFT across sales or transfers.

### What is a realm?

A HyperVIBES realm is an isolated environment with a specific ERC-20 token and various configuration options. Anybody is free to create a realm for their own experiments, protocols, and projects.

### How do I create a realm?

The HyperVIBES dApp (coming soon) can be used to create, view, and manage realms. You can also programmatically create realms directly from the smart contract by invoking the `createRealm` function.

### How do I integrate HyperVIBES into my protocol?

You can use HyperVIBES with any ERC-721 and ERC-20 token without having to write any code or deploy a contract by using the HyperVIBES dApp (coming soon) to manage realms, infuse NFTs, and claim tokens.

More direct integrations can be built by directly invoking the HyperVIBES smart contract from your protocol.

{% content-ref url="developers/integration.md" %}
[integration.md](developers/integration.md)
{% endcontent-ref %}

### How can I infuse an NFT?

You can view all realms that you are allowed to infuse within the HyperVIBES dApp (coming soon). After selecting a specific realm, you can then choose to infuse NFTs based on the constraints and realm configuration.

### How do I claim infused tokens?

You can view all realms that you can claim tokens from in the HyperVIBES dApp (coming soon). After selecting a specific realm, you can then browse the NFTs you own with claimable tokens.

### What NFTs can I infuse via HyperVIBES?

Any ERC-721 NFTs can be infused via the protocol, depending on realm configuration. ERC-1155s cannot be infused.

HyperVIBES is not a minting platform, it was designed to allow infusing tokens into NFTs minted on any platform.

You do not have to use rarible.com NFTs with HyperVIBES.

### What tokens can I infuse via HyperVIBES?

Any ERC-20 tokens can be used with HyperVIBES.&#x20;

Each realm is configured with a single token.

### What does it cost to use HyperVIBES?

HyperVIBES will always be 100% free to use, with zero fees, forever.

### Is there a protocol or governance token?

No, there is no upgradeable functionality nor fee extraction. There is nothing to govern on the protocol itself.

Peripheral communities may choose to launch a DAO / token.

### What can I build with HyperVIBES?

Anything you want. The only limit is your imagination.

{% content-ref url="use-cases.md" %}
[use-cases.md](use-cases.md)
{% endcontent-ref %}

### Can an NFT be infused with multiple tokens?

Yes, a single NFT could be infused across an infinite number of realms and mining several tokens simultaneously.

Depending on how a realm is configured, an NFT may be infused multiple times (from multiple agents) in the same realm.

### Do you have to own the NFT to infuse it?

This depends on the realm configuration.

### How can I contribute?

Hang out in the [Rarible DAO Discord](https://discord.gg/ZtZqH7nfgG)! We're working to make a habit of shipping fun and highly-composable decentralized software like HyperVIBES.

{% content-ref url="developers/links-and-repos.md" %}
[links-and-repos.md](developers/links-and-repos.md)
{% endcontent-ref %}
