# 🏄♀ Dive In

Welcome to **HyperVIBES**.** **

This page will walk you through using the HyperVIBES protocol on the **Goerli Test Network**:

* 🦊 Get your browser setup with a web3 wallet ([https://metamask.io/](https://metamask.io))
* 🚰 Request some test tokens on the Goerli network ([https://faucet.paradigm.xyz/](https://faucet.paradigm.xyz))
* 🤑 Deploy your own ERC-20 token ([https://coinmechanic.io/](https://coinmechanic.io))&#x20;
* 🎨 Deploy a custom ERC-721 NFT contract ([https://wemint.art/](https://wemint.art))&#x20;
* 🛸 Create a HyperVIBES realm ([https://app.hypervibes.xyz](https://app.hypervibes.xyz))
* 🌈 **Infuse your NFTs **&#x20;

{% hint style="info" %}
You might have done some of these steps already. That's cool! This guide covers every point in the process so you can jump in and out where it makes senes.&#x20;

**HyperVIBES is all about experimentation.**&#x20;
{% endhint %}

{% content-ref url="../use-cases.md" %}
[use-cases.md](../use-cases.md)
{% endcontent-ref %}

### Overview

**HyperVIBES** is a public and trustless protocol for infusing tokens inside of any NFT.&#x20;

Infused tokens can be mined and claimed by the NFT owner over time.

{% content-ref url="../README (1).md" %}
[README (1).md](<../README (1).md>)
{% endcontent-ref %}

Today, you're going to launch your own personal ERC-20 token and NFT contract using community-authored tools that are 100% free. Then, you're going to use the HyperVIBES protocol to create your own realm and infuse your NFTs with your token.

{% hint style="info" %}
**This walkthrough will be done on an Ethereum test network**, it won't cost any real money.

These same steps can be taken on any mainnet blockchain as well when you're ready to launch your project.
{% endhint %}

### Setup Your Wallet

If you haven't already, install MetaMask, an in-browser extension that allows you to connect to blockchain based decentralized applications, or "dApps":

* [https://metamask.io](https://metamask.io)

MetaMask will allow you to interact with Ethereum-based networks and testnets, as well as networks like Polygon and Arbitrum.

{% hint style="info" %}
First time setting up metamask? [**Here is an official guide**](https://metamask.zendesk.com/hc/en-us/articles/360015489531-Getting-started-with-MetaMask)
{% endhint %}

Make sure you have selected the **Goerli Test Network** from the network dropdown menu at the top of the MetaMask window.

### Drip Some Funds

A testnet "faucet" is a simple app that will send you tokens and NFTs on various test blockchains. You can skip this step if you already have tokens and have used the Goerli testnet before:

* [https://faucet.paradigm.xyz](https://faucet.paradigm.xyz)

In order to prevent abuse, you must log in with Twitter. After logging in, provide your wallet address from your MetaMask in the input to deliver test funds to your account.

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 1.46.55 PM (1).png>)

### Deploy Your Token

Deploy your own ERC-20 token via CoinMechanic. If you already have a token you'd like to use, you can skip this step.

* [https://coinmechanic.io](https://coinmechanic.io)

This could be a social token, community token, governance token... or anything else you could imagine.&#x20;

{% hint style="info" %}
**You could also use any existing ERC-20 token** (such as ENS, MIST, or USDC) for your realm -- but check your local jurisdiction's securities law before you get too crazy.
{% endhint %}

#### Deploy

Select **Build Token** from the CoinMechanic site, setup your token however you wish:

![Token Builder UI](<../.gitbook/assets/Screen Shot 2021-11-15 at 1.30.24 PM.png>)

Once your token has been deployed, you can easily add it to your MetaMask. The initial supply will have been minted to your wallet:

![Token deployed screen](<../.gitbook/assets/Screen Shot 2021-11-15 at 1.33.11 PM.png>)

{% hint style="info" %}
**Notice the Contract address for your token** -- this is needed later when you configure your HyperVIBES realm.
{% endhint %}

### Deploy Your NFT Contract

Deploy your own ERC-721 via wemint.art. If you already have minted NFTs or have your own contract, then you can skip this step.

* [https://wemint.art](https://wemint.art)

Controlling your own contract is a powerful way of establishing provenance around the pieces you mint.

{% hint style="info" %}
**You can use any existing ERC-721 NFTs as well**, HyperVIBES works across all minting platforms.

Depending on how you configure your realm, you don't even need to own the NFTs to infuse them.
{% endhint %}

#### Deploy

Make sure to **CONNECT** your wallet to the wemint.art app via the button in the top right, and ensure you are still on the **Goerli Test Network**. Provide some basic info to deploy your ERC-721 contract:

![wemint.art site](<../.gitbook/assets/Screen Shot 2021-11-15 at 1.40.39 PM.png>)

Once the contract is deployed:

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 1.57.09 PM.png>)

{% hint style="info" %}
**Notice the contract address once deployment has finished**, you'll need this later when setting up your realm.
{% endhint %}

#### Mint

Select **HOW TO** in wemint.art for a basic walkthrough of getting artwork into IPFS. Alternatively, you can use the following metadata URI:

* `ipfs://ipfs/QmPVEKvFEm9CHPzrKBuj7CPiEML9jKRUap7Lbpxu4tC1ce`

Once you have your metadata URI, select the **MINT** tab, provide the contract address and metadata URI:

![Minting in wemint.art](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.05.22 PM.png>)

Press **MINT! **and your NFT will be minted!

* [https://testnets.opensea.io](https://testnets.opensea.io)

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.16.54 PM.png>)

### Create Your Realm

Previously, we have:

* Created our own ERC-20 token and minted some initial supply of tokens to our wallet
* Created our own ERC-721 NFT contract and minted a single NFT to our wallet

Now it's time to setup a HyperVIBES realm!

* [https://app.hypervibes.xyz](https://app.hypervibes.xyz)

Ensure you are still on the **Goerli Test Network**, and select the first card:

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.18.42 PM.png>)

We will create our realm by inputting all the various configuration information. How you configure your realm is up to you!

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.19.13 PM.png>)

We can leave admin blank for now, as we don't need to modify this realm. After press **NEXT**, add the NFT contract you deployed earlier as the **Allowed Collection: **

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.19.30 PM (1).png>)

And set the **TOKEN ADDRESS** to the ERC-20 we deployed earlier (confirm the token symbol on the right of the input box):

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.20.05 PM (1).png>)

asdf

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.20.17 PM.png>)

sadf

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.20.27 PM.png>)

Once you press **CREATE REALM**, submit the transaction!

Once your transaction goes through, select **INFUSE** from the top menu.

### Infuse

Once you've created your realm, visit the INFUSE section via the top menu. You should see your newly created realm there:

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.26.20 PM.png>)

If you don't see it, confirm the transaction went through and that you are still on the Goerli network. Sometimes it can take a few moments for TheGraph to index new realms as well.

Select your realm, and then select your collection:

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.26.25 PM.png>)

Once you select your collection, type in Token ID **0** to infuse the token we minted previously:

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.26.32 PM.png>)

Then input any amount of tokens you want to infuse, based on how you've configured your realm previously. These tokens will be transferred from your wallet into the NFT:

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.26.43 PM.png>)

If this is your first infusion, you'll have to execute the **APPROVE** step as part of the standard ERC-20 approval flow:

![](<../.gitbook/assets/ .png>)

Once the approval completes, you can infuse your NFT!

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 2.38.28 PM.png>)

Your NFT is now infused!

### Claiming Tokens

TODO

### Sharing Your Token

TODO
