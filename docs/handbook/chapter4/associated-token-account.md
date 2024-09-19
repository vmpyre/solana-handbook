## Associated Token Account

An Associated Token Account (ATA) is a special account on Solana that is used to store tokens from SPL Token Program.

!!! important

    An ATA is derived from its **owner's wallet address** and the **address of the mint**.

This means that user has a different ATA for every wallet and token mint combination. This is very convenient because programs can easily find and interact with the correct account without needing the user to provide the address.

!!! info

    A user can receive tokens even if they do not yet have a token account for that mint. The **sender is able to fund the creation of the receiver's ATA**, enabling things like airdrop campaigns.

[Associated Token Account Program](https://spl.solana.com/associated-token-account) facilitates the creation and management of ATAs.
