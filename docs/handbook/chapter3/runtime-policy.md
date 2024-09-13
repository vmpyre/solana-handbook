## Runtime Policy

Runtime policy is a set of rules enforced by the Sealevel runtime to ensure security of the system:

1. Account ownership can only be changed by the account owner:
    - The account must be **writable**.
    - The account must **not be executable**.
    - The data must be **zero-initialized or empty**.
2. An account not owned by the program cannot have its balance reduced.
3. The balance of read-only and executable accounts may not change.
4. Only the owner can modify account size and data:
    - The account must be **writable**.
    - The account must **not be executable**.
5. Making an account executable is an irreversible operation that can only be done by the account owner.
6. No one can modify the **rent_epoch** associated with this account.

## Compute Budget

Each transaction is allocated a compute budget to prevent abuse of node resources that could potentially lead to network failures or denial of service. When the program consumes its entire compute budget or exceeds certain bounds, the runtime halts the currently running instructions and returns an error.
