But First, Coffee --- Revenue Intelligence Analysis

Project Overview

This project evaluates But First, Coffee (BFC) from a
revenue-management perspective using externally observable competitive,
menu, promotional, customer-review, store-access, and channel data.

The central business question is:

How can But First, Coffee grow profitable revenue without
compromising affordability?

Because internal transaction, product-cost, labor-cost, and
contribution-margin data were not available, the project does not
estimate BFC's actual profitability. Instead, it identifies observable
revenue opportunities, tests selected competitive pricing evidence,
models revenue scenarios, and defines the internal data required for
management validation.

Business Objectives

The analysis focuses on four management areas:

Competitive Pricing --- determine how BFC's pricing compares
with Starbucks Philippines and The Coffee Bean & Tea Leaf
Philippines using directly comparable products.

Promotion Economics --- evaluate the unit-volume response
required for discounts to maintain revenue.

Customer Experience --- identify the customer-experience
dimensions most frequently mentioned in collected reviews.

Revenue Opportunities --- translate external evidence into
management tests related to pricing, promotions, basket building,
operational execution, and commercial access.

The revenue framework used throughout the project is:

Revenue = Transactions × Average Transaction Value

with:

Average Transaction Value = Average Selling Price × Items per
Transaction

For an internal extension:

Contribution Margin = Selling Price − Variable Cost

Research Questions

RQ1 --- Competitive Market Position

How does But First, Coffee's competitive market position compare with
Starbucks and CBTL in terms of menu variety, pricing, store presence,
and customer access channels?

RQ2 --- Individual Customer Ratings

Is there a statistically significant difference in individual customer
ratings among But First, Coffee, Starbucks Philippines, and The Coffee
Bean & Tea Leaf Philippines?

Cross-brand inference was not performed because the verified
individual-rating sample contained only 13 BFC observations and no
comparable individual-rating samples for Starbucks or CBTL. Aggregate
branch ratings were not treated as independent customer observations.

RQ3 --- Customer Experience

Which customer experience factors are most frequently associated with
positive and negative customer experiences across the three coffee
brands?

Customer-experience themes are primarily interpreted descriptively.
Review mention prevalence is not treated as a dissatisfaction rate, and
no causal claims are made from review text.

Analytical Workflow

The project follows a reproducible analytics workflow:

Business Understanding
        ↓
Data Collection
        ↓
Data Cleaning & Validation
        ↓
Exploratory Data Analysis
        ↓
Statistical Analysis
        ↓
Revenue Opportunity Analysis
        ↓
Tableau Preparation
        ↓
Executive Dashboard

Notebook Structure

notebooks/
├── 00_business_understanding.ipynb
├── 01_data_collection.ipynb
├── 02_data_cleaning.ipynb
├── 03_exploratory_data_analysis.ipynb
├── 04_statistical_analysis.ipynb
├── 05_revenue_opportunity_analysis.ipynb
└── 06_tableau_preparation.ipynb

Data

Competitive Menu Dataset

The analytical menu sample contains 150 observations:

But First, Coffee: 50

Starbucks Philippines: 50

The Coffee Bean & Tea Leaf Philippines: 50

Equal row counts do not imply equal menu composition. For that
reason, whole-menu averages are descriptive and were not used as the
main inferential competitive-price comparison.

Customer Reviews

The collected review dataset contains 282 reviews:

Starbucks: 108

But First, Coffee: 104

CBTL: 70

A review can contain multiple customer-experience themes.

Individual Ratings

Only 13 verified individual Google-origin ratings were available,
all for BFC. These were summarized descriptively and were not used for
cross-brand statistical inference.

Key Findings

1. Competitive Pricing

BFC's collected beverage menu had a median price of ₱130.

To reduce menu-composition bias, five directly comparable beverage
families were matched across the three brands:

Product Family         BFC   Starbucks      CBTL

Americano             ₱130        ₱175      ₱185
Café Latte            ₱150        ₱185   ₱187.50
Caramel Macchiato     ₱130        ₱210      ₱245
Matcha Latte          ₱130        ₱190      ₱225
Mocha                 ₱150        ₱205      ₱220

Across these matched families, BFC's mean family-level percentage price
gap was:

28.2% below Starbucks

34.1% below CBTL

These percentages are mean matched-family price gaps, not whole-menu
price differences.

2. Statistical Pricing Evidence

A Friedman test was used because the three brands were compared across
the same five matched product families.

Friedman result:

Q(2) = 10.00

p = 0.0067

The result indicates an overall difference in price rankings across the
three brands.

BFC ranked lowest in price across all five matched families. However,
exact pairwise Wilcoxon signed-rank tests were not statistically
significant after multiple-comparison adjustment. The overall result
therefore should not be interpreted as proof that every individual brand
pair differs significantly.

3. Promotion Economics

In the collected BFC menu snapshot:

45 of 50 products displayed promotional pricing

Observed promotion coverage: 90%

Observed discount: 20%

This is a snapshot of observed promotional coverage and should not be
interpreted as BFC's permanent promotion strategy.

A 20% discount requires a 25% increase in unit volume to maintain
the same revenue:

Required Volume Lift = [1 / (1 − Discount)] − 1

For a 20% discount:

[1 / 0.80] − 1 = 25%

This represents revenue neutrality, not profit neutrality.

4. Customer Experience

Among the 104 collected BFC reviews, the management dimensions with
the highest mention prevalence were:

Management Dimension           Mention Prevalence

Product Quality                             50.0%
Packaging                                   19.2%
Value & Portion                             19.2%
Order Execution                             15.4%
Availability & Consistency                  13.5%
Customization & Add-ons                     12.5%
Service & Delivery                           7.7%
Loyalty Experience                           3.8%

These percentages represent review mention prevalence, not complaint
rates or dissatisfaction rates. A dimension can be mentioned positively,
negatively, or in another context.

5. Review Polarity Context

The conservative polarity rules classified 147 of 282 reviews
(52.13%).

Overall polarity distribution:

Unclear: 47.87%

Negative: 38.65%

Positive: 12.41%

Mixed: 1.06%

Among reviews where explicit polarity could be identified, 74.15%
contained negative evidence without identified positive evidence.

This should not be described as a population-level dissatisfaction rate
because nearly half of the reviews remained unclassified under the
conservative rules.

Revenue Opportunity Framework

The project identifies five management opportunities. Their order is a
presentation sequence and not a priority ranking.

Selective Pricing

Revenue mechanism: Average Transaction Value

BFC's matched-family affordability position suggests a hypothesis that
selected products may have pricing headroom. The appropriate management
action is controlled price testing rather than a broad price increase.

Promotion Optimization

Revenue mechanism: Transactions + Average Transaction Value

Promotions should be evaluated based on incremental demand and
contribution rather than promotional sales volume alone.

Basket Building

Revenue mechanism: Average Transaction Value

The external menu sample supports a basket-building hypothesis involving
complementary items, food, or add-ons. The menu sample is not a
substitute for actual transaction-basket data.

An illustrative scenario using a ₱130 beverage and ₱50 incremental
item produces approximately 7.7% modeled ATV growth at a 20%
attachment rate.

This is a scenario, not observed BFC customer behavior.

Operational Execution

Revenue mechanism: Transactions + Retention

Customer-experience dimensions such as product quality, packaging, order
execution, availability, and consistency identify areas for deeper
operational investigation and possible revenue-leakage analysis.

Commercial Access

Revenue mechanism: Transaction Volume

Observed delivery, payment/partnership, physical-access, and expansion
capabilities can be evaluated with internal channel economics to
determine whether each channel generates incremental and profitable
transactions.

Scenario Analysis

Selective Pricing

Using the matched BFC average price of ₱138, illustrative price
scenarios were modeled from 0% to 10%.

A price increase can tolerate some unit-volume decline while maintaining
revenue, but revenue neutrality alone does not determine whether the
change improves contribution margin or customer economics.

Promotion Response

For a 20% discount:

Unit Volume Increase   Revenue Change

                  0%             -20%
                 10%             -12%
                 20%              -4%
                 25%               0%
                 30%              +4%
                 40%             +12%
                 50%             +20%

Basket-Building Scenario

Using a ₱130 base beverage and a ₱50 incremental item:

Attachment Rate   Modeled ATV   ATV Change

             0%       ₱130.00        0.00%
             5%       ₱132.50       +1.92%
            10%       ₱135.00       +3.85%
            15%       ₱137.50       +5.77%
            20%       ₱140.00       +7.69%
            25%       ₱142.50       +9.62%
            30%       ₱145.00      +11.54%

These are modeled scenarios and not forecasts of actual BFC performance.

Evidence Hierarchy

To avoid overstating external evidence, findings are separated into five
levels:

Statistical evidence --- matched-family Friedman test

Observed quantitative evidence --- menu prices and observed
promotion coverage

Descriptive customer evidence --- review themes and management
dimensions

Scenario analysis --- pricing, promotion, and basket-response
calculations

Management hypotheses --- actions requiring internal validation

Internal Data Required for the Next Phase

A full internal revenue-management model would require:

POS Transactions

For: - Revenue - Transactions - Average Transaction Value - Items per
transaction - Product mix - Price realization - Branch productivity -
Price elasticity

Product Cost Data

For: - Contribution margin - Contribution margin percentage - Menu
engineering - Product-level profitability

Promotion History

For: - Promotion incrementality - Baseline comparison - Promotion ROI -
Cannibalization - Discount-depth optimization

Order Operations

For: - Revenue leakage - Cancellations - Refunds - Order errors -
Product availability - Preparation time

Customer and Loyalty Data

For: - Purchase frequency - Retention - Repeat behavior - Customer
lifetime value

Channel Performance

For: - Channel-specific revenue - Incremental transactions - Fees and
commissions - Contribution by channel

Dashboard

The project includes an executive revenue-intelligence dashboard
presenting:

BFC beverage median price

Matched price gaps versus Starbucks and CBTL

Observed promotion coverage and discount

Revenue-neutral volume requirement

Matched product-family pricing

Promotion revenue-volume trade-off

Customer-experience mention prevalence

Revenue opportunity framework

Methodology and evidence limitations

An interactive HTML dashboard was also developed for executive
presentation, including responsive visualization, scenario interaction,
and revenue-opportunity tooltips.

Tools and Technologies

Python

Pandas

NumPy

SciPy

Jupyter Notebook

Tableau

HTML / CSS / JavaScript

Git / GitHub

Python was used for data preparation, validation, exploratory analysis,
statistical testing, scenario modeling, and dashboard-data preparation.

Project Structure

but_first_coffee_revenue_analysis/
├── data/
│   ├── raw/
│   └── cleaned/
├── notebooks/
│   ├── 00_business_understanding.ipynb
│   ├── 01_data_collection.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_exploratory_data_analysis.ipynb
│   ├── 04_statistical_analysis.ipynb
│   ├── 05_revenue_opportunity_analysis.ipynb
│   └── 06_tableau_preparation.ipynb
├── outputs/
│   ├── figures/
│   └── tables/
├── tableau/
├── dashboard/
├── README.md
├── requirements.txt
└── .gitignore

Methodological Limitations

This project uses external competitive and customer-review evidence. The
following limitations should be considered when interpreting the
findings:

Actual BFC sales transactions were unavailable.

Product-level cost and contribution-margin data were unavailable.

Observed promotional pricing represents a collected snapshot, not a
longitudinal promotion history.

Competitive menus differ in composition.

Only five directly comparable beverage families were used for
matched-price inference.

The individual-rating dataset was insufficient for cross-brand
statistical testing.

Customer-review mention prevalence does not measure dissatisfaction.

Store-footprint evidence came from sources with different
definitions and should not be used to calculate market share.

Scenario analyses demonstrate economic relationships and are not
forecasts.

External evidence cannot establish BFC's actual price elasticity,
promotion incrementality, branch profitability, or customer lifetime
value.

Management Interpretation

The external evidence suggests that BFC occupies a strong affordability
position relative to the two benchmark brands within the matched
beverage families.

The appropriate revenue-management response is not automatically to
raise prices or reduce promotions. Instead, the findings support
controlled management tests designed to determine:

where selective pricing improves contribution without unacceptable
volume loss;

which promotions generate genuinely incremental demand;

which basket-building interventions improve ATV and contribution;

where operational execution may protect repeat transactions; and

which commercial channels generate incremental economic value.

The final decision should be based on internal transaction and cost
evidence.

Author

Dr. Jan Noel Vero

Data Analytics | Revenue Management | Hospitality & Tourism |
Business Analysis

Disclaimer

This project is an independent analytical exercise based on externally
collected information. It is not an official analysis commissioned or
endorsed by But First, Coffee, Starbucks Philippines, or The Coffee Bean
& Tea Leaf Philippines. Brand names are used solely for comparative
analytical purposes.