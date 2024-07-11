# Design Document

## Financial Records Schema Design

### Common Fields

Maintain a separate password protected DB for each user.

- id: Unique identifier for the record.
- type: Indicates the type of record (income, expense, investment).
- date: Date of the transaction or record creation.
- amount: Numeric value representing the financial amount involved (positive for income, negative for expenses or investments).
- description: Description or note explaining the transaction.

Handle currency as part of UI.

### Specific Fields

#### Income

- Category: Recurring or not
- Source
- Mode of Income: Which bank account or whether cash.

#### Expense

- Category: Recurring or not
- Source
- Mode of Payment

#### Investment

- investment_type: Stocks, MF
- Broker

## Other Schema Designs

We will maintain some other things as well

### Bank Balance

Just keep store of the bank balance per bank. Will need to allow some for of tallying with the financial records later on.

- id
- name
- balance
- balance update date

### Investment Broker Records

Per broker here. Basically, just a sum of how much money has been invested per broker and current value of the portfolio (will need to be updated by the user)

- id
- name
- portfolio value
- portfolio value update date

## High level diagrams

### System Context
<img title="System Context" alt="System Context" src="./Diagrams/finance-tracking-system-context-diagram.drawio.svg">

### Container Diagrams
<img title="Backend Container Diagram" alt="Backend Container Diagram" src="./Diagrams/backend-container-diagram.drawio.svg">

## Low level diagrams

Skipping designing the UML class diagrams will take too much time and is unnecessary for a single dev (me).
