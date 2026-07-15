# 🏦 Smart ATM Simulator

An interactive command-line interface (CLI) application that simulates real-world ATM operations. Built with Python, this project highlights advanced **Nested `if` statements**, variable updates, and secure user input parsing to mimic authentic hardware interaction steps.

---

## 🎯 Project Objectives
* **Deeply Nested Logic:** Handling consecutive operational checkpoints (Authentication ➔ Operation Choice ➔ Balance Verification).
* **State Management:** Tracking and updating the real-time `balance` variable dynamically after financial transactions.
* **Type-Safe Input Design:** Managing the PIN credential as a string to prevent runtime crashes from unexpected character inputs.

---

## 🗺️ Logic & Decision Tree

```text
[Enter PIN]
   ├── Correct PIN ➔ [Select Operation]
   │                      ├── Option 1: Withdraw ➔ [Enter Amount]
   │                      │                            ├── Amount <= Balance ➔ Dispense Cash & Update Balance
   │                      │                            └── Amount > Balance  ➔ Reject (Insufficient Funds)
   │                      └── Option 2: Check Balance ➔ Display Current Balance
   └── Incorrect PIN ➔ Reject & Exit



💻# Sample Runs
##Successful Cash Withdrawal

=== Welcome to Smart ATM Simulator ===
Please enter your PIN: 1234

Correct PIN! Authentication successful.

Please select an operation:
1. Withdraw
2. Check Balance
Enter choice (1 or 2): 1

Enter the amount you want to withdraw: 1500
Success! Please take your cash.
Your remaining balance is: 3500 EGP

##Unsuccessful Access (Incorrect PIN)

=== Welcome to Smart ATM Simulator ===
Please enter your PIN: 9999

Incorrect PIN. Transaction cancelled.
