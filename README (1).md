# 🛸 Overview

**HyperVIBES** is a public and trustless protocol for infusing tokens inside of any NFT.&#x20;

Anyone can create a realm, which is a fully configurable and isolated environment within the protocol. Depending on realm configuration, infused tokens may be claimed by the owner of the NFT over time.

{% hint style="info" %}
****[**Rarible DAO**](https://discord.gg/ZtZqH7nfgG)** built this protocol as a **[**global public good**](https://newsletter.banklesshq.com/p/global-public-goods-and-the-protocol) to enrich the broader NFT ecosystem, encourage experimentation, and foster creative innovation.

HyperVIBES works with all ERC-721 NFTs, you do not have to mint on rarible.com.
{% endhint %}

### Provenance Mining

The core mechanism at the heart of HyperVIBES is **Provenance Mining**.

ERC-20 tokens can be infused inside of any ERC-721 NFT. Infused tokens are mined over time based on realm configuration, and only the owner of the NFT can claim the currently mined tokens to their wallet.

If the NFT is sold or transferred to another owner, unclaimed tokens stay within the NFT.

{% hint style="info" %}
Provenance mining tokenizes of the act of holding an NFT over time.
{% endhint %}

{% content-ref url="protocol/infusion.md" %}
[infusion.md](protocol/infusion.md)
{% endcontent-ref %}

{% content-ref url="protocol/claiming.md" %}
[claiming.md](protocol/claiming.md)
{% endcontent-ref %}

### Multi-Tenancy

HyperVIBES is a [multi-tenanted](https://en.wikipedia.org/wiki/Multitenancy) protocol. Each isolated tenant is known as a HyperVIBES **realm**.

This means that anybody can permissionlessly create a new realm, with any token they want, configured however they like... without having to fork or deploy a smart contract.

Realms are completely isolated and independent from one another. It's possible for a single NFT to have infused tokens from several different realms.

{% content-ref url="protocol/realms.md" %}
[realms.md](protocol/realms.md)
{% endcontent-ref %}

### Permissionless

There is no gatekeeping or privileged authority within the HyperVIBES protocol.

* Anybody is free to create a realm without permission
* Anybody can infuse any NFT with any token without permission

{% hint style="info" %}
This creates a system of parallel, opt-in, non-coercive and non-rivalrous realms of experimentation layered within any infused NFT.
{% endhint %}

While the protocol itself is not permissioned in any way, individual realms can be configure to limit what agents can infuse or what collections are allowed to be infused, along with several other realm constraints.

### Trustless Infrastructure

There is no administrative functionality nor roles retained by Rarible DAO or any other agent, and the smart contract is non-upgradeable. This ensures that functionality will remain the same for as long as the blockchain exists.

All configured realms are fully sovereign and only modifiable by the admins specified during realm creation.

{% hint style="info" %}
By removing any possibility of rugging or modifying the protocol, other builders do not have to trust Rarible DAO or anybody else when choosing to integrate HyperVIBES.
{% endhint %}

### Extension and Composition

HyperVIBES was designed to be integrated with other protocols and composed within larger on-chain products.&#x20;

A proxy approval system allows external agents to infuse-on-behalf of another address, ensuring that infusions can never be spoofed without explicit authorization while still allowing interesting extensions to the protocol beyond the supported constraints.

{% content-ref url="developers/integration.md" %}
[integration.md](developers/integration.md)
{% endcontent-ref %}
