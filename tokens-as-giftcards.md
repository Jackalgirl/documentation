# Why Tokens Are More Like Giftcards
I have to start off with a big caveat: not all blockchain protocols work in the way I'm about to describe.  But Bitcoin, the mother chain, does, and so does the x-chain in Avalanche, which is the home of Lamina1.  So I feel like there is some usefulness in talking about this.

### The Blockchain is an Immutable Ledger

When I say "ledger", I am not talking about the offline (aka "cold") wallet device going by the brand name of "Ledger".  Instead, I'm simply talking about a record. It's a reference to accounting: accountants keep track of accounts using ledgers.  Ideally, if they are not engaged in shenanigans, their ledgers are _immutable_, meaning that they are written in ink and cannot be changed.

A blockchain is like this.  It is a continuous record of transactions that cannot be edited or deleted, except that it is handled by software, on computer nodes, that are following a common protocol to decide what is, or isn't, a valid addition to the entry.  They work on these in collections of transactions, called "blocks".  A blockchain is a chain of these blocks, all strung together by markers so that readers of the record can follow each transaction back to its source.

### So How do Tokens Work?

A token is just something that's represented in a transaction, associated with an owner or originator (such as in the case of a contract that might create -- mint -- a token) as an entry in the ledger.  In most cases, there are no separate "coins" or "tokens" that somehow exist independently of these ledger entries.  The ledger entry may include metadata such as (in the case of an NFT) the location of a file, but the entry itself is just a ledger entry, like writing down the balance of your bank account in an accounting ledger.

If there are no separate _things_ to be managed or sent, then what happens?  The answer is that again, it's just a ledger entry.  The ledger contains an entry that associates 5 MAGUFFIN tokens with an address, so from the perspective of the network, the address has 5 MAGUFFIN tokens.

### The Double-Spend Problem

So if all of this is just entries in a ledger, there has to be a way to cook the books, right?  To initiate a transaction to spend some quantity of tokens, and while the validators are still working on that block, initiate another transaction to spend the same tokens, so you end up effectively doubling your buying power?

Satoshi Nakamoto's solution to this makes tokens less like real-world coins or bills and more like gift cards.

Imagine that you had a system that made use of gift cards that could only ever be filled once, and that had to be spent all at once (you could not spent part of the gift card: it's all or nothing).  Alice has received a deposit of 5 MAGUFFIN tokens, meaning that there is an entry in the blockchain ledger that records a transfer of 5 MAGUFFIN tokens from somewhere (it doesn't matter at this point) to her public key address.  This entry has a unique serial number associated with it (the transaction hash, or ID).

In the gift card analogy, Alice has received a gift card worth 5 MAGUFFIN tokens, with its unique serial number.  Now she wants to send 2 MAGUFFIN tokens to Bob.  Her card can only be _completely_ spent; she cannot use part of the card.

So here is how it works: Alice surrenders her gift card to a clerk in the system (that is, she submits a transaction request to a blockchain validator).  The clerk marks the card as spent (that is, a new entry appears in the blockchain ledger registering the unique transaction ID as spent).  Now the clerk issues _two new cards_, with new serial numbers that are created in such a way that they are tied to the original serial number.  One of them is worth 2 MAGUFFIN tokens and the other is worth 3 MAGUFFIN tokens.  The clerk forwards the 2-MAGUFFIN card to Bob (meaning: the blockchain now registers an incoming deposit associated with Bob's account that is marked by this new transaction ID) and gives the 3-MAGUFFIN card to Alice as her change.

In this manner, the double-spend problem is avoided, because the original gift card was marked as spent _first_, and used as the origin of two new gift cards, which were then distributed to their owners, Alice and Bob.
