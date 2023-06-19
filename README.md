# Smart-Contract-For-A-Multi-Sig-Wallet
MultiSig Contract
This repository contains a Solidity contract for a multi-signature (multisig) wallet, implemented using the Ethereum blockchain. The contract allows a predefined set of owners to collectively manage and approve transactions.

Contract Details
The MultiSig contract is a multisig wallet that requires a specified number of owners to approve a transaction before it can be executed. Here are the main components of the contract:

Owners and Required Signatures
owners: An array of Ethereum addresses representing the owners of the multisig wallet. These addresses have the authority to confirm and execute transactions.
required: The minimum number of owner signatures required to approve a transaction.
Transactions
transactions: An array that stores the details of submitted transactions, including the destination address, value, execution status, and additional data.
Transaction struct: Defines the structure of a transaction, containing the destination address (_dest), value (_value), execution status (executed), and additional data (data).
Functions
addTransaction: Internal function used to create and add a new transaction to the transactions array.
transactionCount: Public function that returns the total number of submitted transactions.
confirmTransaction: Public function for owners to confirm a specific transaction by providing its ID.
getConfirmationsCount: Public function that returns the number of confirmations received for a given transaction.
submitTransaction: External function for submitting a new transaction, automatically confirming and executing it.
receive: Fallback function that allows the contract to receive Ether.
isConfirmed: Public function that checks if a transaction has received the required number of confirmations.
executeTransaction: Public function used to execute a confirmed transaction.
