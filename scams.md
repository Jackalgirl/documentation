# Common Scams in the Blockchain Industry

## Universally common scams

### The Wallet-Draining Contract
The scammer will attempt to 
convince you that the solution to your problem is to connect a wallet interface that supports such blockchains (typically MetaMask or TrustWallet), link to a website 
("dapp", "node dapps", etc), and then approve a contract that is authorized to spend tokens without limit (also known as "unlimited spend").  The scammer will commonly
refer to this as "rectifying" or "resolving" your wallet.  The contract then automatically drains your wallet of all of the tokens in its contract.  These contracts 
can be revoked by connecting to [Revoke.Cash](https://revoke.cash).

### The Sweeper Contract
Similar to the Wallet-Draining Contract, above; however, this contract automatically transfers out any of the network's native tokens (the 
ones used to pay for gas) to an account under the scammer's control.  Because revoking contracts requires tokens to pay the gas fees, **these contracts cannot be revoked**.

### Stealing your Seedphrase -  this scam involves the scammer attempting to get your account's seed phrase from you.  
See the article ["The Importance of Seed/Mnemonic Phrases in Crypto/Blockchain"](seed-phrases.md) for more information on why this is such a vulnerability.  In this scam, the scammer  will do this either by claiming that 
they need to verify your seed phrase against their records (which is not a thing) or that they need this in order to be able to help you.  Alternately, they will tell you that 
you need to connect to a fake Bittensor wallet site and import your account with your seed phrase, which is indeed how you import your account into a **genuine** wallet interface, 
but their website will be a fake website designed to steal your seed phrase.  Once they have this, they'll hijack your account and steal your tokens.

### Ooops, I Revealed MY Seedphrase
The scammer will post a seedphrase, usually as a screenshot, sometimes under the guise of asking for help. They are hoping that you will be 
greedy and try to hijack their account using this seedphrase.  You will discover that the account has a large quantity of tokens ready for the taking. However, these will not be native 
tokens; they will be tokens deployed by a contract, which means that in order to transfer them out, the account will need to have a quantity of the native network token in order to pay
for gas. But this wallet will not have any of those, meaning that in order to steal the available tokens, you will need to transfer some native tokens in. It will be at this point (possibly
after several attempts to deposit gas tokens) that you will discover that the account has deployed a [sweeper contract](#the-sweeper-contract).

### Pig-Butchering
This involves someone striking up a "relationship" with you, and eventually moving the conversation to investment.  It always involves a completely fake investment website that will 
report that your investments (of the real assets that you send) growing by leaps and bounds, encouraging you to invest more, to enlist your friends & family, etc.  But when you try to 
withdraw your earnings, suddenly there are problems: you have to pay fees, or taxes, or some kind of additional payment, which will continue until you realize that you have been 
scammed, or the scammers ghost you.  Tragically, this very huge industry often involves trafficked persons: people who are modern-day slaves, and who are threatened and beaten if 
they do not comply with the scam.

### The Romance Scam
Similar to [Pig-Butchering](#pig-butchering), this scam involves someone striking up a "relationship" with you, but instead of encouraging you to invest, the scammer simply invents
emergencies or other crises in order to get you to send money.  The crises will never end.

### The Sextortion Scam
A variation of [the Romance Scam](#the-romance-scam) in which a scammer will strike up a "relationship" with you, and then trick you into sending intimate images of yourself, at which
point they will threaten to send these images to your family, friends, and co-workers unless you pay them.  They may promise to delete the images if you pay them, but they will 
of course not do this: they will continue to demand money.  **Do not allow yourself to be blackmailed**: simply block the scammer.

### Invite to DM
A non-moderator, usually new user, not a regular contributing member posts a reply along the lines of "I have a solution for this but can't post links, DM/PM me 
for a guide".  The "guide" will be a link to something that supports one of the above scams.

### Moderator/Admin Impersonation
A scammer will copy all of the profile details of a moderator and approach you in a private conversation. The profile's contents may be convincing,
but the actual username will not match (or may not be present; for example, in Telegram, an imposter may hide their username and copy the moderator/admin's username in their "Bio" in 
the hope that you will not notice that the username is not labelled "username").

### Fake "support"
A scammer will approach you in a private message, claiming to be "support".  No one associated with Lamina1 will ever approach you via private message like this, 
so it is safe to assume that 100% of all PMs/DMs/calls on any social media platform **is a scam**.

### Investment "Education"
The scam typically is phrased as "I'll help x people earn [an unrealistic amount of money in a short amount of time], but you have to share x% of the profit with me".  This is a variation 
of [the Pig-Butchering scam](#pig-butchering).  Once you pay the required percentage of the "profit", you will discover that your "investments" do not exist.

### The Employment "Opportunity"
Scammers will post employment "opportunities" in the form of "we're looking for employees for a crypto project". It will typically be a new user making the posting, and will
invite job-seekers to send them a direct/private message. The scam will typically involve some form of credentials/identity theft, and may involve something similar to the 
[fake check](#fake-check-scam), or an "opportunity" to launder funds as a [money mule](#money-mule).

### The Fake Conversation
A pair of accounts, typically brand new ones, start posting a "conversation" in public. It may jump straight to promoting the scam, or there may 
be some initial entirely fake conversation happening before it gets to the promotion of the actual scam. Since it's usually a single scammer copying and pasting from a script, if you are around long enough, you'll see the same conversation between different accounts. Sometimes they will involve some outrageously silly topic (such as one of them announcing that their girlfriend won the "Swedish Rock & Roll Dance Championships") to attract attention.

### The Scam After
If you have been scammed, scammers will target you for a follow-on scam by promising to hep you "recover your funds" or "recover your account". This will be especially 
effective if you have lost a large quantity of assets or the control of an important account: they will exploit your strong desire to believe that you can be made whole
and will go to any lengths to reassure you that this can happen. But it is just another scam, seeking to piggy-back on the success of the previous scam.

## Platform-specific scams: Discord

### Fake "Ticket" Discord Servers
A scammer will post a reply, or send you a direct message (DM) and tell you that you need to "open/raise a ticket" or "reach out to the admin" on another Discord server. Once on that 
server, the scammer will attempt to convince you to approve a [wallet-draining contract](#the-wallet-draining-contract) or a [sweeper contract](#the-sweeper-contract). It is also 
common for the scammer to send you to this server via the [Discord Redirect](#discord-redirect) in an attempt to steal your login credentials.

### Discord Redirect
The scammer will invite you to log into another Discord server.  When you click on the invite, "Discord" will ask you to login again, or the verification 
bot will send you to a "login website".  But it isn't Discord -- just a fake version of Discord.  Once you have provided them your login credentials, the site will route you to 
the server, so that it looks like you've logged in and joined the server.  But now the scammers have your Discord credential.  **Always set up 2FA with social media platforms, 
including Discord**.

### Spoofed Roles
The scammer will use emojis to try to spoof server roles in the "About Me" or "Pronouns" section of their bio. These roles will appear in their profile if they start up 
a direct message (DM) conversation with you, but specific server roles *will not show up in direct messages*, because they are associated with that particular server (and 
when you are in a DM, you are not in the server).

## Platform-specific scams: Telegram

### Fake Channels
By default, your Telegram settings will authorize anyone to add you to a channel. Scammers will frequently join a legitimate channel and then add its members to a copy-cat fake
channel (which will be almost identical to the official channel), in which they will announce scam "opportunities" to "claim rewards/airdrop tokens" in order to get you to link 
to their scam site and approve a [wallet-draining contract](#the-wallet-draining-contract) or a [sweeper contract](#the-sweeper-contract).  You can protect yourself frmom this by 
editing your settings: 
o Go to "Privacy and Security"
o Select "Group & Channels"
o Set this to "My Contacts"

### Spoofed Usernames
The scammer will copy the username of a legitimate moderator/admin/core team member into the "Bio" field of their profile, hoping that you will not notice that the username is not
labelled as "username".

## Why This is Effective
### "Do Your Own Research"
If you're new to the industry, there are a lot of technical aspects about it that you might not yet know. You will frequently be told to "DYOR" ("Do Your Own Research"), but this
is also a skill (that no one is born with) that is something that must be learned to do properly. Many people feel shame admitting that they do not know something (yet), and so 
they will not, but this will leave them in a state of ignorance that a seemingly-confident, reassuring scammer can exploit.  Or, a person will admit ignorance, but if they have
not yet learned *how to research*, may again be taken in by a helpful and willing "teacher". 

### Hurry, Hurry, Hurry
There is a great sense of "Fear of Missing Out" (FOMO) in the blockchain/cryptocurrency industry, which is carefully cultivated by scammers and people who are using this relatively unregulated
space to take people's money. Scammers will exploit this with copy-cat sites, channels, and links, trusting that you will be in such a rush that you will not notice that there is
something wrong with the link (the link itself is not quite right) or the nature of the offer (it's not in keeping with how the project has operated in the past).

### The Universal Need for Certainty and Assurance
Scammers will project a front of confidence, helpfulness, and reassurance. They will often attempt to take on the identity of someone trustworthy, and will frequently have references
to trust, honesty, helpfulness, faith, etc., in their bios, profiles, and display names. 

## How to Protect Yourself

### Asking Questions in Open Chat is NOT RESEARCH
Learning where to find official, accurate information is the *first thing you should
learn to do.* Asking questions in open chat means that you are relying on someone else to interpret information for you, and this is only as good as the person answering you. If you
are new to a project, then *you will not yet know who is answering you*, which makes you vulnerable to any confident, reassuring scammers who are on the lookout for potential
victims.

Get in the habit of looking for the official announcements channel or site, a "Frequently-Asked-Questions" document, and take some time to review the official
sources of information such as websites & documentation library. Note only does this give you something to verify any claims you see, but also gets you a sense of the project's goals
and the way it operates, which will help you more quickly recognize when something happens that does not feel right.

Spend some time lurking in open chat also, to get a sense of who the official moderators/administrators are and who the community regulators are. This will help you recognize 
situations such as completely new users inviting you to move your conversation to private or direct channels (out of the view of actual moderators)

### Acknowlege Your Own Limitations
You are not a fundamentally bad person if you don't know something - you just don't know it yet.  You're also not a stupid person if you don't know it (no one is born with this 
knowledge).  And it's particularly difficult to know what you don't know.
So one of the most powerful (but difficult) things you can do is 
recognize that you are vulnerable (even if you are convinced that you are not), and to handle this by training yourself to *slow down* and ask yourself the following questions whenever you see an
opportunity:
o Is it coming from an official site/announcement? (Know how to find those)
o Is it coming from an official person (Know how to validate those)
o Does this seem typical behavior for the project? (Be familiar enough with the project to recognize this; if you do not know, *slow down* and take some time to investigate)

### Learn How to Spot Fakes
o Know where to locate the official contract addresses of any tokens you might be looking to buy, sell, or trade.
o Know how World-Wide-Web (WWW) domain names work; for example, subdomains are separated from the parent domain **only by periods**, and no other character, so `airdrop-project.com` is 
not the same as `airdrop.project.com`.  In the former, `airdrop-project.com` is the *entire domain name*, whereas in the latter, `airdrop` is a subdomain of `project.com`.  Why is this
important?  Anyone can register a domain name, but only the holder of a specific domain name can add subdomains.
o Be familiar with how profiles or bios work in social media platforms so that you can more easily recognize spoofed roles, badges, tags, or usernames.

### Resist Pressure to Act Swiftly
Anyone telling you that you must act swiftly. Legitimate offers will usually have a bigger timeframe to participate, because projects want their communities to participate. Pressure to
act quickly is a tactic used by scammers in order to shut down your caution/critical-thinking skills. **If you are being pressured to act quickly, that is precisely the time to slow 
down and look more carefully.**

