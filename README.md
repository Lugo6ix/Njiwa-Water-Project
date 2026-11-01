# Njiwa Water Project: Power BI Dashboard

A Power BI dashboard that tracks a water-access improvement program: how many improvements are complete, how much has been spent against budget, where and on what the money went, and how many people now have basic water access.





## Business problem

Njiwa has a critical shortage of safe drinking water. Sources are contaminated or poorly distributed, and the limited number of public taps leads to queues of more than 30 minutes. The program needs to show progress and spending clearly to two audiences.

**Members of the public want to see:** how the project is going, how much has been spent, where and on what, and details about their own province.

**Decision-makers also want to see:** whether there is enough money to finish, where costs can be cut, and data at national, provincial, and town level.



## Findings

|Metric|Value|
|-|-|
|Total population|28M|
|Population with basic water access|about 13M (47.83%)|
|Improvements complete|21.61% (5,488 of 25,399)|
|Improvements in backlog|about 20K (19,911)|
|Cost of completed improvements vs budget|$33.79M vs $30.52M (about 10.7% over)|
|Largest cost by improvement type|Install RO filter, $14.3M (about 42%)|

## Data

Source: \[dataset source or course name]. The Excel workbook has seven tables used in the model:

|Table|Rows|
|-|-|
|water\_source|39,650|
|location|39,650|
|visits|60,146|
|well\_pollution|17,383|
|project\_progress|25,399|
|infrastructure\_cost|12|
|vendors|95|

## 

## Data cleaning (Power Query)



* Corrected misspelled project statuses and improvement names
* Standardized water source types and capitalization, and trimmed extra spaces
* Removed unused columns
* Set correct data types



## Data model



Seven tables connected by six relationships: project progress, visits, and well pollution link to water source; project progress also links to infrastructure cost and vendors; visits link to location.



## Key measures (DAX)

* Budgeted cost: unit cost, multiplied by 1.5 for rural towns
* Cumulative cost and cumulative budget by completion date
* Percent of improvements complete
* Population with basic water access (clean well, home tap, or shared tap with queue under 30 minutes, plus improved sources)
* Aggregated improvements (groups 1 to 8 tap installs into "Install Public Taps")
* Average queue time and project duration



## Recommendations



* Review RO filter costs first: they are the largest spend and the program is over budget.
* Re-estimate the budget for the remaining backlog before committing more funds.



## Files

* screenshots: dashboard screenshots
* `Njiwa\_Water\_Project.pbix`: the Power BI report file
* `data/`: a small sample of the data 





## Author



Hafeez Olakotan | linkedin.com/in/hafeezol

