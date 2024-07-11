# Requirements

Basically, all the things I want in the thing at a high level. The point of this project is to be able to tell me where my money is and how much money I have in my back accounts and investments.

## Contents

1. Rough Ideas
2. Functional Requirements
3. Non-functional Requirements

## Rough Ideas

- Only intend to use it as a single user platform, but I'll still include multi-user support and authentication.
- Only tracks finances, no super confidential details such as passwords. Will keep the financial data also secured in a way.
- Want a web-based UI for simplicity and will be using it only on my desktop, so the question of reponsive design does not come up.
- I want to be able to track
    1. Income
    2. Expenses
    3. Investments

    Across multiple bank accounts.
- Should look like a spreadsheet. Actually, I'll just add like a small diagram of how I want it to look like.

## Functional

1. User Authentication
    - The system should support user authentication (why am I even writing this?).

2. Dashboard
    - The dashboard should provide an overview of
        1. Total money in my bank accounts
        2. Total money spent
        3. Total money invested and money gained on them
    - It should display summaries for multiple bank accounts.
    - It should display all views (incomes, etc.) as one with the option for selecting each/multiple views. A view is a table.
        - The user should be able to add tags, sort of like a notion table.
        - Views are paginated with support for filtering and searching (Semantic search, that's the main reason I want to make my own).
    - Add charts to track investments and expenditure and net worth over time.
    - Wev-based UI

3. On each of the views
    - Allow support for recurring increments/deductions.
    - And of course, indvidual viewing, addition, changing and deletion.
    - The view should add a shortened description of the actual description using an LLM summarizer.
    - Categorizing through tags.

4. Investments
    - Add special tags for the place (Ex - trading account) where you made the investment.
    - Allow updating current value of portfolio management.
    - (Maybe) scrape the place where you made the investment and show growth, but that is too farfetched.

## Non-functional

1. Security
    - For authentication
    - While storing financial data.

2. Performance
    - Handle large number of records

3. Usability
    - I should be able to use it easily, yeah, that's it.
