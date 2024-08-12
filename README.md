 Hot Potato Module
Overview
Manages a simple wallet system with loan functionality and a non-storable HotPotato resource.

Key Components
Wallet:

Structure: Stores a balance.
Functions:
create(account: &signer): Initializes a wallet with a balance of 100.
HotPotato:

Structure: An empty struct that can't be dropped, cloned, copied, or stored.
Loan Functions:

Loan from Wallet: loan_from_wallet(addr: address, amount: u64) -> (Wallet, HotPotato)

Purpose: Withdraws amount from the specified wallet and returns the loaned amount along with a HotPotato.
Pay Loan: pay_loan(addr: address, loan: Wallet, hot_potato: HotPotato)

Purpose: Deposits the loan amount back into the wallet, verifies balance, and destructs the loan and HotPotato.