# Coffee Shop Sales Dashboard (Excel)

![Coffee Shop sales dashboard](Coffee%20shop%20sales%20DashBoard.png)

An interactive Excel dashboard that shows when, where and what a multi-location coffee shop sells. It covers about $698K in sales across roughly 149K transactions, with filters for month and day of week.

**Tools:** Excel (Power Query, PivotTables, PivotCharts, slicers)
**Domain:** Retail, food and beverage analytics

---

## Business problem

A coffee shop chain wants to staff the right number of people at the right hours, stock the products that sell, and understand why some stores outperform others. This dashboard turns raw sales records into answers to those questions.

## Questions the dashboard answers

1. How much do we sell, and what is the average bill?
2. Which hours of the day are busiest?
3. Which product categories and individual products earn the most?
4. How do sales vary by day of the week?
5. Which store performs best on traffic and revenue?
6. How are orders split by size?

## Dataset

- **Source:** Coffee Shop Sales raw data (a public practice dataset, included as `Coffee Shop Sales (raw data).xlsx`)
- **Size:** about 149K transactions
- **Main fields:** transaction date and time, store location, product category and name, quantity, unit price, size
- **Note:** this is a sample dataset, not data from a real business.

## Approach

1. **Clean** the raw data in Power Query: fix data types, check for blanks and duplicates, create hour, weekday and month fields.
2. **Define the metrics** (see below) so each number has one clear meaning.
3. **Analyze** with PivotTables for sales by hour, day, store, category and product.
4. **Visualize** with PivotCharts and KPI cards on one dashboard sheet, with slicers for month and day.

## Metric definitions

| Metric | Definition |
|---|---|
| Total sales | Sum of quantity × unit price across all transactions (about $698K) |
| Footfall | Number of transactions, with each transaction counted as one customer visit (about 149K) |
| Average bill | Total sales ÷ number of transactions (about $4.69) |

## Key findings

| Area | Finding |
|---|---|
| Sales and traffic | About $698K from about 149K transactions, a high-volume, low-ticket business with an average bill of about $4.69 |
| Peak hours | Demand peaks between 7 and 10 AM |
| Categories | Coffee earns about 39% of revenue, followed by Tea and Drinking Chocolate |
| Top products | Barista Espresso, Brewed Chai Tea, Gourmet Brewed Coffee |
| Stores | Hell's Kitchen leads on both traffic and revenue, with Lower Manhattan close behind |
| Weekdays | Strong Monday to Friday traffic, with a noticeable drop on Saturday |
| Order size | Large, Regular and Undefined orders each make up roughly a third |

Read these as patterns in the sample data, not as proven causes.

## Recommendations

These are hypotheses for a store manager to test, based on what the dashboard shows.

1. **Staff for the 7 to 10 AM peak.** Put the strongest shifts and enough stock in place before the morning rush.
2. **Protect the core menu.** Coffee drives about 39% of revenue, so availability of the top three products matters most.
3. **Look at Saturday.** The weekday pattern points to commuter and office demand, though that is an inference. Check Sunday figures and test a weekend promotion before concluding anything.
4. **Benchmark stores on more than totals.** Hell's Kitchen leads, but compare average bill and sales per hour across stores to see whether it wins on traffic, ticket size or both.
5. **Understand "Undefined" before using order size for upselling.** A third of orders have no size, which may simply be items that don't come in sizes, so it is not yet an upsell signal.

## Limitations

- The dataset has no cost or margin data, so I can describe revenue but not profit.
- There are no customer IDs, so repeat-customer behavior can't be measured. A transaction is treated as a visit.
- The "Undefined" size group is unexplained in this analysis.
- The data is a sample covering a limited period, so seasonal conclusions are not possible.

## Next steps

- Add average bill and sales per hour by store.
- Build a day-of-week by hour heatmap.
- Break down the product mix by hour, for example hot vs cold drinks.
- Investigate what the "Undefined" size group contains.
- Rebuild the dashboard in Power BI and compare it with this Excel version.

## Repository contents

```
├── Coffee Shop Sales (raw data).xlsx          # raw dataset
├── pivot + dashboard coffee shop sales.xlsx   # PivotTables and dashboard
├── Coffee shop sales DashBoard.png            # dashboard screenshot
├── Coffee Shop Sales Analysis.pdf             # exported report
└── README.md
```

**To explore:** download `pivot + dashboard coffee shop sales.xlsx`, open it in Excel, and use the slicers on the dashboard sheet to filter by month and day.

## Skills demonstrated

Data cleaning (Power Query) · PivotTables and PivotCharts · KPI and metric definition · Dashboard design with slicers · Retail sales analysis · Turning findings into recommendations

## Author

**Bharat Sinha**, aspiring data analyst
[LinkedIn](https://www.linkedin.com/in/bharat-sinha-122791130/) | [GitHub](https://github.com/bharat-sinha) | sinha.bharat8@gmail.com
