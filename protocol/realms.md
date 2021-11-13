# 🌎 Realms

HyperVIBES is a [multi-tenanted](https://en.wikipedia.org/wiki/Multitenancy) protocol where anybody is free to create a **realm**, which is an isolated environment that can be configured and used independently from other realms.

Permissionless creation of realms allows anybody to build any protocol, experiment, or project on top of HyperVIBES without interfering with anybody else or asking for permission.

{% hint style="info" %}
This also means that **most use cases for HyperVIBES can be implemented without having to write any custom code** nor deploy a smart contract
{% endhint %}

{% content-ref url="../use-cases.md" %}
[use-cases.md](../use-cases.md)
{% endcontent-ref %}

### Realm Configuration

When a new realm is created, the following information is provided:

* **name** - Display name for the realm. Does not have to be unique across HyperVIBES.
* **description** - Description for the realm.
* **ERC-20 token** - The specific token that can be infused into NFTs for this realm.
* **token daily mining rate** - How many tokens per day each NFT will mine once infused.
* **realm constraints **- Configuration of the parameters of the realm. _See below._
* **admins** - Addresses that are allowed to add or remove **admins**, **infusers**, **claimers**, or **collections** to the realm.
* **infusers** - Addresses that are allowed to infuse NFTs. Ignored if the **allow public infusion** constraint is true.
* **claimers** - Addresses that are allowed to claim mined tokens from an NFT. Ignored if the **allow public claiming** constraint is true.
* **collections** - NFT contract addresses that can be infused. Ignore if the **allow all collections** constraint is true.

{% hint style="info" %}
When a realm is created, an **id **will automatically be assigned.
{% endhint %}

{% hint style="warning" %}
Realm name, description, token, constraints, and daily mining rate **cannot be modified once the realm is created.**

You can always create additional realms (potentially with the same token) if you want to use different parameters in your project.
{% endhint %}

### Realm Constraints

Realm constraints determine the behavior around infusing, claiming, and token mining. By creating realms with different constraint configurations, a wide range of possible applications can be implemented.

* **min infusion amount** - An NFT must be infused with at least this amount of the token every time it's infused.
* **max token balance** - An NFT's infused balance cannot exceed this amount. If an infusion would result in exceeding the max token balance, amount transferred is clamped to the max.
* **min claim amount** - When claiming mined tokens, at least this much must be claimed at a time.
* **require NFT is owned **- If true, the infuser must own the NFT at time of infusion.
* **allow multi infuse **- If true, an NFT can be infused more than once in the same realm.
* **allow public infusion** - If true, anybody with enough tokens may infuse an NFT. If false, they must be on the **infusers** list
* **allow public claiming** - If true, anybody who owns an infused NFT may claim the mined tokens. If false, they must be on the **claimers** list
* **allow all collections **- If true, NFTs from any ERC-721 contract can be infused. If false, the contract address must be on the **collections** list.
