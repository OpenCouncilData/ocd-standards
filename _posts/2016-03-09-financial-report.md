---
category: Financial
path: '/financialreport'
title: 'Financial report'
---
## Financial report 0.1 (draft for comment)

**([Comments welcome!](https://github.com/okfnau/open-council-data/issues))**

A financial report is a collection of spreadsheets put out each year by a council reporting on its financial activities over the previous financial year. It includes a balance sheet, income and expenditure statements, capital works programme and so on.

Several states have standard (Microsoft Excel based) formats in which these reports are written and submitted to a central authority. The OpenCouncilData standard given here is a machine-readable (CSV) format that closely mirrors the [Victorian Local Government Model Financial Report](http://www.dtpli.vic.gov.au/local-government/publications-and-research/planning-and-reporting). Councils in other states should follow a similar process for their state's model financial report, if it exists.

Each of the different components of the report (balance sheet, capital works programme etc) should be published as a separate CSV file. We recommend publishing them all as resources (files) within a single dataset (CKAN package), for open data platforms that support that kind of structure.

**Important**: unlike the Excel-based format, CSV files should *not* include any subtotals such as "Total income" or "Total non-current assets".

CSVs are grouped such that all the numeric values within one file have the same "direction", and can thus be meaningfully summed. For example, liabilities must be subtracted from assets, so they are in a separate file.

* All values should be in thousands of dollars. (That is, `300` means $300,000)
* Do not include $ signs or commas.
* Remember that category names containing commas must be enclosed in double quotes: `"Plant, machinery and equipment"`

### Balance sheet - assets

This is the template to be followed, with a sample value of $1,234,000 for the first item. `2016` should be replaced with the current year, and `1234` represents the actual value that would be included (in thousands of dollars). Multiple years can be included as additional columns.

```
Category, Item, 2016
Current assets,Cash and cash equivalents,1234
Current assets,Trade and other receivables
Current assets,Other financial assets
Current assets,Inventories
Current assets,Non-current assets classified as held for sale
Current assets,Other assets
Non-current assets,Trade and other receivables
Non-current assets,Investments in associates and joint ventures
Non-current assets,"Property, infrastructure, plant and equipment"
Non-current assets,Investment property
Non-current assets,Intangible assets
```

### Balance sheet - liabilities

```
Category, Item, 2016
Current liabilities, Trade and other payables
Current liabilities, Trust funds and deposits
Current liabilities, Provisions
Current liabilities, Interest-bearing loans and borrowings
Non-current liabilities, Provisions
Non-current liabilities, Interest-bearing loans and borrowings
```

### Balance sheet - equity

```
Category, Item, 2016,
Equity, Accumulated surplus
Equity, Reserves
```

### Statement of Capital works

```
Category, Item,2016
Property,Land
Property,Land improvements
Property,Buildings
Property,Heritage Buildings
Property,Building improvements
Property,Leasehold improvements
Plant and equipment,Heritage plant and equipment
Plant and equipment,"Plant, machinery and equipment"
Plant and equipment,"Fixtures, fittings and furniture"
Plant and equipment,Computers and telecommunications
Plant and equipment,Library books
Infrastructure,Roads
Infrastructure,Bridges
Infrastructure,Footpaths and cycleways
Infrastructure,Drainage
Infrastructure,"Recreational, leisure and community facilities"
Infrastructure,Waste management
Infrastructure,"Parks, open space and streetscapes"
Infrastructure,Aerodromes
Infrastructure,Off street car parks
Infrastructure,Other infrastructure
```

### Statement of Capital Works - summary

```
Category, Item,2016
Represented by,New asset expenditure
Represented by,Asset renewal expenditure
Represented by,Asset expansion expenditure
Represented by,Asset upgrade expenditure
```

### Comprehensive Income Statement – income

```
Category, Item, 2016
Income,Rates and charges
Income,Statutory fees and fines
Income,User fees
Income,Grants - operating
Income,Grants - capital
Income,Contributions - monetary
Income,Contributions - non monetary
Income,"Net gain (or loss) on disposal of property, infrastructure, plant and equipment"
Income,Fair value adjustments for investment property
Income,Share of net profits (or loss) of associates and joint ventures 
Income,Other income
```

### Comprehensive Income Statement – expenses
```
Category, Item, 2016
Expenses, Employee costs
Expenses, Materials and services
Expenses, Bad and doubtful debts
Expenses, Depreciation and amortisation
Expenses, Borrowing costs
Expenses, Other expenses
```

### Statement of Cash Flows
```
Category, Item, 2016
Cash flows from operating activities,Rates and charges
Cash flows from operating activities,Statutory fees and fines
Cash flows from operating activities,User fees
Cash flows from operating activities,Grants - operating
Cash flows from operating activities,Grants - capital
Cash flows from operating activities,Contributions - monetary
Cash flows from operating activities,Interest received
Cash flows from operating activities,Dividends received
Cash flows from operating activities,Trust funds and deposits taken
Cash flows from operating activities,Other receipts  
Cash flows from operating activities,Net GST refund/payment
Cash flows from operating activities,Employee costs
Cash flows from operating activities,Materials and services
Cash flows from operating activities,Trust funds and deposits repaid
Cash flows from operating activities,Other payments
Cash flows from investing activities,"Payments for property, infrastructure, plant and equipment"
Cash flows from investing activities,"Proceeds from sale of property, infrastructure, plant and equipment"
Cash flows from investing activities,Payments for investments
Cash flows from investing activities,Proceeds from sale of investments
Cash flows from investing activities,Loans and advances made
Cash flows from investing activities,Payments of loans and advances
Cash flows from financing activities,Finance costs
Cash flows from financing activities,Proceeds from borrowings
Cash flows from financing activities,Repayment of borrowings
Cash flows from financing activities,Net increase (decrease) in cash and cash equivalents
Cash flows from financing activities,Cash and cash equivalents at the beginning of the financial year
```

### Statement of Changes in Equity
Additional years can be included as extra rows.

```
Year,Item,Total,Accumulated Surplus,Revaluation Reserve,Other Reserves
2016,Balance at beginning of the financial year
2016,Surplus/(deficit) for the year
2016,Net asset revaluation increment/(decrement)
2016,Transfers to other reserves 
2016,Transfers from other reserves
```