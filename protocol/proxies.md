# 💼 Proxies

Proxies are an advanced HyperVIBES mechanic that ensures that on-chain customization is possible for more complex integrations with the protocol.

This allows developers to launch a HyperVIBES realm with complete control over the infusion and claiming experience.

{% hint style="info" %}
You can [**configure a realm**](realms.md)** **with various constraints directly in the HyperVIBES UI **with no need for custom smart contracts**.

Proxies are only needed for advanced integrations.
{% endhint %}

{% content-ref url="../use-cases.md" %}
[use-cases.md](../use-cases.md)
{% endcontent-ref %}

### Overview

A HyperVIBES **proxy** is an address that an agent has delegated infusion and claiming functionality to.

Once an agent (the delegator) has delegated to a proxy, the proxy may now:

* **Infuse tokens into an NFT on behalf of the delegator**. Infused tokens must come from the proxy's address, and the delegator will be recorded as the infuser.
* **Claim infused tokens from NFTs owned by the delegator**. Claimed tokens are sent to the proxy's address.

#### Design Rationale

It can be useful to have a smart contract "frontend" to the infusion or claiming steps to add custom functionality for a realm beyond the built-in constraints.&#x20;

However, we do not want to allow any contract to have the ability to attribute infusion nor claim tokens on behalf of an addresses without that address giving explicit authorization.&#x20;

{% hint style="info" %}
This ensures that no matter how the realm is configured,** nobody can "spoof" the recorded infuser nor claim tokens without permission. **
{% endhint %}

### Allowing and Denying Proxies

The `allowProxy` and `denyProxy` functions on the HyperVIBES smart contract are used to add and remove proxies on behalf of the message sender.

From `IHyperVIBES.sol`:&#x20;

```solidity
    // allower operator to infuse or claim on behalf of msg.sender for a
    // specific realm
    function allowProxy(uint256 realmId, address proxy) external;

    // deny operator the ability to infuse or claim on behalf of msg.sender for
    // a specific realm
    function denyProxy(uint256 realmId, address proxy) external;
```

These functions will allow or deny `proxy` the ability to infuse and claim on behalf of `msg.sender`.

You can view and query proxy information from the HyperVIBES subgraph.

{% content-ref url="../developers/subgraph.md" %}
[subgraph.md](../developers/subgraph.md)
{% endcontent-ref %}
