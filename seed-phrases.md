# The Importance of Seed/Mnemonic Phrases in Crypto/Blockchain

One of the main points of blockchain technology is to allow people to conduct transactions without having to rely on a central authority.  This means, there is no central server/authority/system 
checking to make sure, when someone submits a transaction request to the network, that the entity making that request is the legitimate owner of the account in question. So how does the blockchain know that 
the request you're making is actually coming from you?

When you use a seed or mnemonic phrase to make a wallet, there is a one-way algorithm that uses the phrases to generate a public and private key.  
Anyone can see your public key -- it's often your address, or your public key shown in another format.  But the blockchain will only obey people who can prove they have the public and 
private key (that's what a signature is).

That's it, though.  That's the only way the blockchain knows whether a request is legitimate.   It has no idea who you are.  All it wants to know is: are the keys correct? 

So if you give someone your seed phrase, they can use it to regenerate your public and private keys, and they can sign requests (like transferring away all your tokens) and the 
blockchain has no way of knowing that it's not you.

If you give someone your seed phrase, you can change all the passwords you want, delete the apps off of your phone or browser, keep your cold wallet device like a Ledger disconnected 
from the Internet: none of that matters.  Any wallet application can regenerate the keys as long as it's given the seed phrase, and then sign transactions and the 
blockchain will be none the wiser.

Wallet-generating apps usually only store the seed phrase in the temporary memory of your device (phone, computer, browser) for as long as it takes for you to confirm that yes, you have 
written this down and stored it somewhere safely.  Once you're past this step, the wallet apps will clear the memory.  If you have any questions as to whether your wallet application allows
you to access the Seed/Mnemonic Phrase, or the private key that's generated using the Phrase, **check with your wallet application's official support**.  If you ask about this in public, 
you may get approached by people claiming to be "support" or offering to "help" you, but these **will always be scammers**.

So anyone telling you that there is some central database of phrases that they are looking at in order to verify you have the right one are liars.  **Anyone telling you they need 
this info to "verify your account" is a liar**
