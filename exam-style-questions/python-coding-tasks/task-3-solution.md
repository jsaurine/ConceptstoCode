# Task 3 Solution

```python
# Simple Transaction Ledger
# This program tracks income and expenses, and stores them in a file.
# It loads past transactions at startup and saves new ones when exiting.

import datetime  # for timestamps
import os  # for file existence check

# ------------------------
# FUNCTION DEFINITIONS
# ------------------------

def load_ledger(filename):
    """
    Load transactions from a file into a list.
    
    Returns:
    - A list of transactions, each a dictionary with keys: date, description, amount
    """
    ledger = []
    if not os.path.exists(filename):
        return ledger  # No file yet, return empty list

    with open(filename, "r") as file:
        for line in file:
            # Each line is: date,description,amount
            parts = line.strip().split(",")
            if len(parts) == 3:
                date, description, amount_str = parts
                try:
                    amount = float(amount_str)
                    ledger.append({
                        "date": date,
                        "description": description,
                        "amount": amount
                    })
                except ValueError:
                    print(f"Skipping invalid line: {line.strip()}")
    return ledger

def save_ledger(ledger, filename):
    """
    Save the list of transactions to a file.

    Parameters:
    - ledger (list): List of transaction dictionaries
    - filename (str): File to write to
    """
    with open(filename, "w") as file:
        for transaction in ledger:
            line = f"{transaction['date']},{transaction['description']},{transaction['amount']}\n"
            file.write(line)

def add_transaction(ledger):
    """
    Prompt the user to enter a transaction and add it to the ledger.

    Parameters:
    - ledger (list): The transaction list to append to
    """
    description = input("Enter transaction description: ").strip()
    while True:
        try:
            amount = float(input("Enter amount (positive = income, negative = expense): "))
            break
        except ValueError:
            print("Invalid amount. Please enter a number.")

    date = datetime.date.today().isoformat()  # Format: YYYY-MM-DD
    ledger.append({
        "date": date,
        "description": description,
        "amount": amount
    })
    print("Transaction added.")

def display_summary(ledger):
    """
    Display all transactions and current balance.

    Parameters:
    - ledger (list): The transaction list
    """
    if not ledger:
        print("No transactions found.")
        return

    print("\n--- Transaction Summary ---")
    balance = 0
    for i, t in enumerate(ledger, start=1):
        print(f"{i}. {t['date']} – {t['description']} – ${t['amount']:.2f}")
        balance += t["amount"]
    
    print(f"\nCurrent balance: ${balance:.2f}")

# ------------------------
# MAIN PROGRAM
# ------------------------

def main():
    filename = "ledger.txt"
    ledger = load_ledger(filename)  # Start with existing transactions

    print("Welcome to the Simple Transaction Ledger!")

    while True:
        print("\nMenu:")
        print("1. Add a transaction")
        print("2. Show all transactions and balance")
        print("3. Exit and save")
        
        choice = input("Choose an option (1–3): ").strip()
        if choice == "1":
            add_transaction(ledger)
        elif choice == "2":
            display_summary(ledger)
        elif choice == "3":
            save_ledger(ledger, filename)
            print("Ledger saved. Goodbye!")
            break
        else:
            print("Invalid choice. Please select 1, 2 or 3.")

# Run the program
main()

```
