# Customer Lifetime Value
:round_pushpin: **GOAL :** 
> Define customer lifetime value

# <h4>Tools & Others</h4>

[![](https://img.shields.io/badge/tools-miro-rgb(244,208,63)?style=f?style=flat-square&logo=miro&logoColor=white)](https://miro.com/)
[![](https://img.shields.io/badge/OS-Mac-green?style=f?style=flat-square&logo=macos&logoColor=white)](https://www.apple.com/macos/ventura/)
[![](https://img.shields.io/badge/OS-Windows-green?style=f?style=flat-square&logo=windows&logoColor=white)](https://www.microsoft.com/)
[![](https://img.shields.io/badge/Git_Update-26_Jun_2023-brightgreen?style=f?style=flat-square&logo=github&logoColor=white)](https://github.com/)

#
**Customer Lifetime Value**
> **Definition :** Customer Lifetime Value or CLV is calculated as a single dollar number, CLV summarizes total revenue and costs related to a customer over time, CLV provides a net profit/loss summary, or more usually on average value for a customer within a particular market segment
>
> CLV is an important measure of customer profitability and usually considered to be a very important marketing metric, because of the range of the marketing objectives it measures within a single number.

<br>

<h3>Simple Customer Lifetime Value (CLV)</h3> <br>

```ruby

CLV = AvTransactionPerMonth*AvOrderValue*AvGrossMargin*AvCustomerLifespanInMonths

## Example ###
  AvTransactionPerMonth = Total_transaction{Number_of_months}/Period{Number_of_months}
  AvOrderValue = Total_Revenue{July}/Number_of_orders{July}
  AvGrossMargin = ( ( Total_Revenue{July}-Discounts{July} )/Total_Revenue{July} )*100

  AvCustomerLifespanInMonths = 1/Churn_Rate

## Note ##
  Churn_Rate = ( (Number_of_customer_at_begining_{July})-(Number_of_customer_at_the_end_{July}) )/(Number_of_customer_at_begining_{July})

```

<br>

<h3>Standard Customer Lifetime Value (CLTV)</h3> <br>
- CLV with Time Value of Money

```ruby

CLTV(At_the_begin_of_period) = M/(1+d-r)
CLTV(At_the_end_of_period) = ( M*(1+d) )/(1+d-r)

# with Churn rate

CLTV(At_the_begin_of_period) = ( M*r*(1+d) )/(1+d-r)
CLTV(At_the_end_of_period) = ( M*r )/(1+d-r)

## Note ##
r = retention_rate # Percentage of customers who stay on the platform
d = discount_rate # $100 in 2030 is less than $100 today
M = contribution_margin = ( Total_Revenue{period}/Number_of_customers{period} )-VariableCost_or_spent_in_serving_the_customer)

```

<br>

![Capture1](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/assets/118663358/b68e9ba9-d190-4689-8ec8-56e106402a7d)

<br>

#
Go to top : [Top :world_map:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101/blob/main/Week03_CustomerScoring/week03.md#customer-scoring) <br>
Go to home page ( contents ) : 
[Home :earth_asia:](https://github.com/HikariJadeEmpire/AdvancedAnalytics-MADT8101#advancedanalytics)

