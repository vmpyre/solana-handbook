## Token-2022 Program

The Token-2022 Program extends the functionality provided by the Token Program. This means that the Token-2022 program is not only backward compatible but also includes all the functions of the original Token program, as well as additional functionality often referred to as token extensions.

!!! info

    One associated token account program still creates token accounts for both Token and Token-2022.

## Benefits

- **Flexibility**

    Token issuers can choose to enable any combination of token extensions.

- **Reduced risk**

    Using audited and well-tested extensions helps protect protocols and funds.

- **Reduced testing costs**

    Extensions are added by specifying the extensions in code, this reduces number of errors and saves time on testing.

- **Reduced development time**

    Extensions are uniform and reusable, which significantly speeds up development.


## Extensions

There are two types of extensions:

- **Mint Extensions**
- **Account Extensions**

!!! note

    - **Mint extensions** are added on top of the original Solana Token Program and extend the capabilities of tokens.
    - **Account extensions** are added on top of Solana accounts and add account-related features.

Some of the mint extensions:

- **Confidential transfers**: Allow confidential transfers between participating users without revealing the amount transferred.
- **Transfer fees**: Allow transfer fees to be charged on each transfer and sent to a specified account.
- **Mint close authority**: Allows owners to close mint accounts and reclaim the lamports.
- **Transfer hook**: Allows calling specific programs with each token transfer.

Account extensions  include:

- **Memo required on transfer**: Requires an attached memo as a message during each token transfer.
- **Immutable owner**: Makes it impossible to reassign ownership of an account.
- **Default account state**: Freezes all new token accounts so that users must interact with the project in some way to unfreeze the accounts/tokens.
- **CPI guard**: Restricts how other programs can interact with your token by prohibiting certain actions inside cross-program invocations.

!!! note

    You can find a list of Token-2022 extensions in the [documentation](https://spl.solana.com/token-2022#extensions).
