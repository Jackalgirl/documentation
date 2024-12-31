# Verifying Identity using Signed Messages in Lamina1
**_Why Signing a Message is Useful & How to Do It_**

The Lamina1 Hub supports a feature for signing messages, and for verifying signed messages.  Why might this be useful?

## Identify Verification
The primary use of signing a message is to prove that you are the account's owner.  If you have read the article "[The Importance of Seed/Mnemonic Phrases in Crypto/Blockchain](https://github.com/Jackalgirl/documentation/blob/main/seed-phrases.md)", you may recall that an account consists of two keys: the public key, which anyone can see[^1], and the private key, which is the key that the account's owner uses to authenticate a transaction (or signature).  Because the two keys are linked, a blockchain validator can verify, using the public key, that the transaction was submitted by someone who is in possession of the private key.  With a signed message, you can prove to someone else that you are the owner of your account and, vice versa, they can prove to you that they are the owner of their account.

## When Might this be Useful?
Imagine that someone is offering an NFT or other asset for sale Over the Counter (OTC): this means that they are not using a marketplace or other system designed specially for buying and selling assets.  Instead, they're simply saying, "I have this asset for sale, pay me xL1 and I will transfer it to you," and are typically making the arrangement for this one-on-one with a prospective buyer, either in public or in private.  

This obviously requires a significant amount of trust.  Not only do you, as a potential buyer, have to trust that they will in fact send you the asset once you send them the payment, but you have to trust that they actually have the asset in the first place.

For NFTs in particular: if you are looking at the item's listing in the Lamina1 Hub, you can see its owner.  Take, for example, the FujiKnight NFT, here: 

![Screenshot of an NFT Item on the Lamina1 Hub: "The FujiKnight", an NFT created by Jackalgirl and currently owned by Jackalgirl](./images/JG_The-FujiKnight.png)
_(see this item on the Hub, directly, here: https://lamina1.com/item/0xab4d-fcb8c7-44937851760156022634111755770988795508464617439675138338516243802549346445721)_

If you look at this item, you can see that it is currently owned by Jackalgirl.  Let's say, for example, that Jackalgirl (or someone claiming to be Jackalgirl) claims that they are conducting an OTC sale of this NFT.  One of the things you could do, as a potential buyer, is ask the seller to send you a signed message.  You will be able to verify that this message was signed (or not) by the Jackalgirl account on the Hub; if you can verify it, then you know you are talking to Jackalgirl.  Whether or not she will actually send you the NFT if you pay her is another matter, but at least you know that it's her.[^2]

## How to Sign a Message

First, agree on the _plaintext_ of the message to be signed.  In order to verify a signed message, you must have the _exact_ plaintext message, so take care to select something that isn't potentially ambiguous.

Next, you'll go to the Hub and click on the "Sign Message" icon, which you can find by opening up your details using the triangle next to your account balance.  The icon look like a little scribble of handwriting, and if you hover over it, you will see the "Sign Message" tooltip:

![Screenshot the account details pop-up on a Lamina1 account, with a tooltip that reads "Sign Message" over an icon that looks like handwriting. ](./images/JG_Sign-Message-Icon.png)

## How to Verify a Message



[^1]: The alphanumeric, or "c-chain" address that you see -- the one that starts with "0x" and is a mixture of letters and numbers -- is actually a shorter string of characters _derived_ from the longer public key.
[^2]: Or it's someone who has access to her private key.  You see, the network has no way of distinguishing between the real Jackalgirl and, say, a scammer to whom she has foolishly given her private key or the mnemonic phrase that she used to create her account, because that's the whole point of blockchain: to enable you to execute transactions trustlessly, without requiring identification (the private key _is_ the identification).  So even if you have a signed message, it's important to keep this in mind.  For more on public/private keys, see "[The Importance of Seed/Mnemonic Phrases in Crypto/Blockchain](https://github.com/Jackalgirl/documentation/blob/main/seed-phrases.md)" and "[Common Scams in the Blockchain Industry](https://github.com/Jackalgirl/documentation/blob/main/scams.md)".
