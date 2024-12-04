# What IS a Wallet (and why tokens are NOT "in" your wallet)

A blockchain is simply an uneditable record of information: think of it as a spreadsheet to which authorized users can add rows, but no one can delete or edit previously-added rows once
they are committed to the record.  Validators are the one using a consensus system (they are "agreeing" as to what constitutes a valid addition to the record) to add transactions to 
the ledger in batches, which are also known as "blocks".  They do this sequence, always adding: they keep adding blocks to a continuous chain of blocks -- hence, "blockchain".

### So What IS a "Wallet"?

It's a confusing term, because most of us are very familiar with the physical wallets we might have in our pockets, purses, or bags: these contain actual bills (paper money) or coins 
(metal tokens). We can open up our real world wallets and count the physical pieces of money in there, and so there's a real temptation to think that when you're dealing with 
cryptocurrency, that these are also separate "coins" that are "in" our blockchain "wallet".  

However, **this is not the case**.  There is no place in blockchain tech that "contains wallets" which themselves "contain tokens".
Remember that a blockchain is just a record of transactions that are grouped together (these are the "blocks" that form the chain of blocks, the blockchain). Your "wallet" 
is better termed an *account*, and it is really just a pair of related keys: your public key (usually your address) and your private key.  When you are looking at the balance of your account, 
what your account management application (aka "wallet app") is doing is querying the blockchain for a sum of all of the free tokens accounted for in every transaction -- that is, every 
ledger entry (spreadsheet row) -- that mentions your public key (which haven't been spent).  

There's also an additional tendency to call the applications that we use to submit transactions to the blockchain "wallets", which leads to further confusion: if you have MetaMask, for example, 
the application *is not your account*, and if you are using the word "wallet" to refer to your blockchain account, this means that MetaMask *is not your wallet*.  Rather, it's the piece of 
software that you use to interact with the blockchain's validators, by means of your account's credentials (its public and private keys).

### There Is No ~~Spoon~~ Token

So does this mean that tokens don't really exist?  Well, no, they don't, not in the sense of "chunks of something, like paper or metal, that can be moved around".  They're just quanties
in blockchain transaction records, that reflect token information pulled from its contract address, typically[^1], the current owner, and whether they are unspent (blockchain protocols will also handle
activities like staking in different ways, but these will be reflected as transactions in the blockchain ledger too).

[^1] The main utility token of a blockchain will not usually have a contract address.  It is generated when the first -- genesis -- block of the blockchain is created.

### It's All About the Keys

Blockchain validators do not know who you are, and they're not *supposed* to: the whole point of a "permissionless blockchain" is that the validator should not need to know who *you* are in 
order to accept your transaction, propose it to the network of validators, agree that it's valid and should be processed, and then add it to the blockchain's actual ledger (finalizing it). 
The way they know that the transaction is valid is because, when you use your wallet application to make a transaction request, the application submits the transaction in the form of an encrypted 
message (aka a "hash") as well as the original request.  The application encrypts it using your private key, that it has stored within the application.  The blockchain can compare this hash to a
hash it creates of the message using your **public key**.  Such is the nature of the algorithm that generates these public/private keypairs is that these hashes will end up being the same.  If 
the validator's hash matches the hash your wallet application provided, it accepts the transaction as valid.

This is, by the way, why you should **never ever ever** give anyone a mnemonic/seed phrase (which is what the algorithm uses to generate the keypair) or your private key.  If you do that, they 
can now become you in the eyes of the blockchain validators (remember: they don't care who you are, they just care if you're using the right key).  You could delete every wallet application you 
have, disconnect your computers from the Internet entirely, turn them off or even destroy them, and *it would not matter*; the hijacker will still be able to move your assets elsewhere.

### Recap/Summary

The term "wallet" is misleading in a lot of ways.  Your wallet application (MetaMask, Trust Wallet, Phantom, Talisman, etc) is not your account, and does not contain tokens, NFTs, etc.  
It's a piece of software that allows you to  talk to blockchain validators.  It's the blockchain validators that add (never edit or subtract) to the chain of blocks that makes up the blockchain ledger (its record).  Even if you deleted all 
of your wallet applications, a record of your account and all of its transactions (including its ownership of tokens) will forever be a part of the blockchain's history.
