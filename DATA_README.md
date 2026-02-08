# Data Dictionary

## Dataset: Bank Transactions

### Overview
This dataset contains synthetic banking transaction data spanning 3 months (November 2024 - February 2025) with 100+ transaction records simulating realistic personal finance activity.

### File Information
- **Filename**: `bank_transactions.csv`
- **Format**: CSV (Comma-Separated Values)
- **Records**: 100 transactions
- **Date Range**: 2024-11-01 to 2025-02-05
- **File Size**: ~8 KB

---

## Column Definitions

| Column Name | Data Type | Description | Example Values | Constraints |
|------------|-----------|-------------|----------------|-------------|
| `Transaction_ID` | TEXT | Unique identifier for each transaction | TXN001, TXN002 | PRIMARY KEY, NOT NULL |
| `Date` | DATE | Transaction date in YYYY-MM-DD format | 2024-11-01 | NOT NULL |
| `Description` | TEXT | Merchant or transaction description | STARBUCKS #2847, AMAZON.COM | - |
| `Category` | TEXT | Expense/income category | Dining, Groceries, Housing | - |
| `Amount` | DECIMAL(10,2) | Transaction amount in USD | 5.67, 1450.00 | NOT NULL |
| `Transaction_Type` | TEXT | Type of transaction | debit, credit | CHECK IN ('debit', 'credit') |
| `Account_Type` | TEXT | Account where transaction occurred | Checking | - |
| `Balance` | DECIMAL(10,2) | Account balance after transaction | 2847.33 | - |

---

## Categories

### Expense Categories (Debit Transactions)
- **Dining**: Restaurants, coffee shops, food delivery
- **Groceries**: Supermarkets, grocery stores
- **Shopping**: Retail purchases, online shopping
- **Gas/Fuel**: Gas stations, fuel purchases
- **Utilities**: Internet, cable, phone bills
- **Housing**: Rent, mortgage payments
- **Insurance**: Auto, health, life insurance
- **Healthcare**: Pharmacy, medical expenses
- **Entertainment**: Streaming services, subscriptions
- **Transportation**: Uber, rideshare, public transit
- **Travel**: Hotels, airlines, travel expenses
- **Health/Fitness**: Gym memberships, fitness classes
- **Cash**: ATM withdrawals

### Income Categories (Credit Transactions)
- **Income**: Payroll deposits, salary

---

## Transaction Types

### Debit
- Represents money leaving the account
- Includes all expenses and withdrawals
- Reduces account balance

### Credit
- Represents money entering the account
- Includes income, deposits, refunds
- Increases account balance

---

## Data Characteristics

### Transaction Patterns
- **Payroll**: Bi-weekly deposits of $3,200
- **Rent**: Monthly payment of $1,450 (12th of each month)
- **Utilities**: Monthly recurring charges
- **Subscriptions**: Regular monthly charges (Netflix, Spotify, etc.)
- **Variable Expenses**: Groceries, dining, shopping vary by day

### Balance Information
- **Starting Balance**: ~$2,847
- **Peak Balance**: ~$14,892
- **Lowest Balance**: ~$3,691
- **Average Daily Balance**: ~$8,500

---

## Data Quality Notes

✅ **No Missing Values**: All required fields are populated
✅ **No Duplicates**: Each transaction has a unique Transaction_ID
✅ **Date Continuity**: Transactions span consecutive dates
✅ **Balance Accuracy**: Running balance is mathematically correct
✅ **Valid Categories**: All transactions have valid category assignments

---

## Sample Records

```csv
Transaction_ID,Date,Description,Category,Amount,Transaction_Type,Account_Type,Balance
TXN001,2024-11-01,STARBUCKS #2847,Dining,5.67,debit,Checking,2847.33
TXN003,2024-11-03,PAYROLL DEPOSIT - ACME CORP,Income,3200.00,credit,Checking,5858.80
TXN014,2024-11-12,RENT PAYMENT,Housing,1450.00,debit,Checking,4008.80
```

---

## Usage Guidelines

### For Analysis
- Use `Date` field for time-series analysis
- Group by `Category` for spending breakdown
- Filter by `Transaction_Type` to separate income from expenses
- Use `Balance` for cash flow tracking

### For Visualization
- Pie charts: Category distribution
- Line charts: Balance over time, Income vs Expenses
- Bar charts: Top merchants, Monthly spending by category
- Trend analysis: Day of week patterns, Monthly trends

---

## Data Generation Method

This is **synthetic data** created for portfolio demonstration purposes. The data simulates realistic banking patterns including:
- Regular payroll deposits
- Fixed monthly expenses (rent, insurance, utilities)
- Variable daily spending (dining, groceries, gas)
- Seasonal variations in spending
- Realistic merchant names and transaction amounts

**Note**: This data does not represent real financial information and should be used solely for educational and demonstration purposes.
