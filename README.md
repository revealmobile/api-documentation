# Report API Documentation 

## Access the docs
[Go to the Docs](https://revealmobile.github.io/api-documentation)

## Useful Terminology
- `Project`: logical grouping of 1 or more locations that represent an *Advertiser* in the VISIT Local Platform.
- `Campaign`: logical grouping of 1 or more mobile device audiences created in VISIT Local observed over a specific date range.
- `Visitor`: unique device observed at a target location.
- `Competitor`: locations that have been co-visited by Visitors of a Project.
- `Conversion`: an observation of a device from a Campaign audience at a Project location during the Campaign report period.
## Campaign Segments
Campaign devices are grouped into four `Pre-Campaign Segments`:
1. `Customers`: devices observed at a Project location in the Campaign Pre-Period
2. `Competitors`: devices not observed at a Project location, but were observed at a Competitor location in the Campaign Pre-Period
3. `NeverVisited`: devices not observed at a Project location nor observed at a Competitor location in the Campaign Pre-Period
4. `AllConversions`: devices observed at either a Project or Competitor location.

*The `Campaign Pre-Period` refers to the range of time `n` days leading up to a campaign, where `n` is the number of days since the Campaign start date.*

Any one of the four `Pre-Campaign-Segments` can be further sub-segmented into  `Campaign Segments`. For example, devices in the Pre-Campaign `Customer` segment can be divided into Campaign Segments for AllConversions, Customers, Competitors, and NeverVisited based on visit observations during the Campaign.
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
## Limits
Requests are limited to:
- 10 requests per minute
- 1000 results retrieved per request


