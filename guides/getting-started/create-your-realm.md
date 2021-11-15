# 🛸 Create Your Realm

Previously, you have:

* Created your own ERC-20 token and minted some initial supply of tokens to your wallet
* Created your own ERC-721 NFT contract and minted a single NFT to your wallet

**Now it's time to setup a HyperVIBES realm:**

* [https://app.hypervibes.xyz](https://app.hypervibes.xyz)

A HyperVIBES realm is a completely isolated environment that can be setup with any ERC-20 token. Each project can set up their own realm, configured to meet their needs.

{% content-ref url="../../protocol/realms.md" %}
[realms.md](../../protocol/realms.md)
{% endcontent-ref %}

### Creating your Realm

Ensure you are still on the **Goerli Test Network **(or whatever your preferred testnet is), and select the first card:

![Choose your path](<../../.gitbook/assets/Screen Shot 2021-11-15 at 2.18.42 PM.png>)

Create a realm by inputting all the various configuration information. How you configure your realm is up to you:

![Initial realm configuration](<../../.gitbook/assets/Screen Shot 2021-11-15 at 2.19.13 PM.png>)

You can leave admin blank for now, there's no need to modify this realm. After press **NEXT**, add the NFT contract you deployed earlier as the **Allowed Collection: **

![](<../../.gitbook/assets/Screen Shot 2021-11-15 at 2.19.30 PM (1).png>)

And set the **TOKEN ADDRESS** to the ERC-20 we deployed earlier (confirm the token symbol on the right of the input box):

![](<../../.gitbook/assets/Screen Shot 2021-11-15 at 2.20.05 PM (1).png>)

By specifying your address for **ALLOWED INFUSERS**, and selected the second option above, you will be the only address that can infuse NFTs for this realm.

Provide additional configuration options:

![](<../../.gitbook/assets/Screen Shot 2021-11-15 at 2.20.17 PM.png>)

Specify constraints around claiming tokens:

![](<../../.gitbook/assets/Screen Shot 2021-11-15 at 2.20.27 PM.png>)

Once you press **CREATE REALM**, submit the transaction.
