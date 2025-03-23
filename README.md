# Reputation-Based Lending Protocol

## Overview
The Reputation-Based Lending Protocol is a Clarity smart contract that facilitates under-collateralized loans based on on-chain credit scores. This system enables borrowers to obtain loans with reduced collateral requirements by leveraging their blockchain-based reputation. The protocol dynamically updates user credit scores based on loan repayment behavior and enforces fair and decentralized lending mechanisms.

## Features

### 1. **User Credit Scoring System**
- Initializes user credit scores at a base level.
- Updates scores based on repayment behavior.
- Penalizes defaulters while rewarding timely repayments.

### 2. **Loan Request and Approval**
- Users can request loans based on their credit score.
- Loan terms such as collateral, interest rates, and duration are dynamically calculated.
- The system ensures users do not exceed active loan limits.

### 3. **Loan Repayment**
- Borrowers repay loans with interest before the due date.
- Successful repayments increase credit scores.
- Defaulted loans result in collateral forfeiture and credit score reduction.

### 4. **Governance and Administration**
- Admins can mark loans as defaulted.
- The protocol maintains decentralized, transparent lending mechanisms.

## Smart Contract Functions

### **Public Functions**
- `initialize-score`: Allows users to set up their credit score profile.
- `request-loan`: Enables users to request a loan, provided they meet the credit score and collateral requirements.
- `repay-loan`: Allows users to repay an active loan, updating credit scores and releasing collateral when applicable.
- `mark-loan-defaulted`: Allows the contract owner to mark overdue loans as defaulted.

### **Read-Only Functions**
- `get-user-score`: Retrieves a user's credit score details.
- `get-loan`: Fetches details of a specific loan.
- `get-user-active-loans`: Returns a list of a user's active loans.

### **Private Helper Functions**
- `calculate-required-collateral`: Computes the necessary collateral based on the borrower's credit score.
- `calculate-interest-rate`: Determines the interest rate dynamically.
- `calculate-total-due`: Calculates the total amount payable, including interest.
- `update-credit-score`: Adjusts the borrower's credit score based on repayment success.
- `update-user-loans`: Maintains active loan records for users.

## Deployment & Testing
### **Deployment Steps**
1. Deploy the contract on the Stacks blockchain.
2. Initialize test users and assign them credit scores.
3. Execute loan requests, repayments, and default scenarios.
4. Validate governance and administrative actions.

### **Testing Scenarios**
- Ensuring only eligible users can request loans.
- Validating credit score changes based on repayment performance.
- Testing edge cases for collateral and interest rate calculations.
- Checking default handling and impact on credit scores.

## Future Enhancements
- Integration with decentralized identity (DID) systems for enhanced credit scoring.
- Allow community-driven governance to oversee default resolutions.
- Introduce staking mechanisms to back under-collateralized loans.


