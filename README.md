# Report API Documentation 

## Access the docs
[Go to the Docs](https://revealmobile.github.io/report-api-documentation)

## Useful Terminology
- `Project`: logical grouping of 1 or more locations that represent an *Advertiser* in the VISIT Local Platform.
- `Campaign`: logical grouping of 1 or more mobile device audiences created in VISIT Local observed over a specific date range.
- `Visitor`: unique device observed at a target location.
- `Competitor`: locations that have been co-visited by Visitors of a Project.

## Index metric format
Index value metrics allow a normalized comparison of visitation between two date ranges with fluctuating sample sizes.

Normalization is achieved by taking observed visit counts for each time period (current and base) as a percentage of total visits.

The normalized values are compared on an index-100 scale to arrive at the final index value.

Hypothetical Example:

```$xslt

Base Period: 
    [2020-08-01 - 2020-08-30] 100 observed visits, 1000 visits in the sample
Current Period: 
    [2020-08-01 - 2020-08-30] 110 observed visits, 1200 visits in the sample

Base Normalized = 100 / 1000 = 0.1
Current Normalized = 110 / 1200 = .092

Index value = (0.092 / 0.1) * 100 = 92
```

The above example shows a decreasing trend in visits by 8 index points when accounting for fluctuation in sample size.
[More Info on Index Values](https://bizfluent.com/how-5339534-calculate-index-numbers.html)


