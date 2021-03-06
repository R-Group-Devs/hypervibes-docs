# 💎 Provenance Mining

Provenance mining is a mechanism that allows an NFT to mine ERC-20 tokens over time that the owner of the NFT can claim. Unclaimed tokens stay within the NFT across sales or transfers.

{% hint style="info" %}
**What happens when you tokenize the act of holding an NFT over time?**

[**Create a realm**](realms.md)**,** run your own experiment, and see what happens!
{% endhint %}

{% content-ref url="../use-cases.md" %}
[use-cases.md](../use-cases.md)
{% endcontent-ref %}

### Infusion

**Infusion** is the process of staking ERC-20 tokens from your wallet into an NFT via HyperVIBES.&#x20;

Infused tokens are then mined by the NFT over time at a linear rate as configured in the realm. Mined tokens do not automatically go to the NFT owner's wallet, they must be "claimed" at some point (_see below_).

* Tokens immediately start mining on the same block they are infused.
* If the **require NFT is owned **constraint of the realm is `true`, the infuser must own the NFT being infused.
* If the **allow public infusion **constraint of the realm is `false`, the infuser must be on the list of allowed infusers for that realm.
* If the **allow all collections** constraint of the realm is `false`, the NFT being infused must be from a collection on the list of allowed collections for that realm.
* If the **allow multi infuse** constraint of the realm is `false`, an NFT can only be infused a single time for that realm.
* The amount being infused must be equal to or greater than the **min infusion amount** constraint set in the realm.
* If the infusion would result in a staked token balance for that NFT that is greater than the **max token balance **constraint for the realm, infused amount is clamped (limited) to the **max token balance** amount. If this clamped amount is less than **min infusion amount**, the infusion will fail.
* If the specified infuser is different than the address submitting the transaction, the infuser must have approved the sender as an [**authorized proxy**](proxies.md)** **ahead of time.

{% content-ref url="../guides/getting-started/infuse-your-nfts.md" %}
[infuse-your-nfts.md](../guides/getting-started/infuse-your-nfts.md)
{% endcontent-ref %}

### Claiming

**Claiming** is the act of withdrawing mined tokens from an infused NFT to the NFT owner's wallet.&#x20;

Only mined tokens can be claimed, while un-mined tokens stay staked within the NFT. Unclaimed tokens stay within the NFT across sales or transfers.

* The total amount being claimed must be equal to or greater than the **min claim amount** constraint set in the realm.
* It is possible to claim less than the total claimable amount if desired.
* If the **allow public claiming** constraint of the realm is `false`, the claimer must be on the list of allowed claimers for that realm.
* If the address submitting the claim transaction does not own the NFT, the NFT owner must have approved the sender as an [**authorized proxy**](proxies.md)** **ahead of time

{% content-ref url="../guides/getting-started/claim-tokens.md" %}
[claim-tokens.md](../guides/getting-started/claim-tokens.md)
{% endcontent-ref %}
