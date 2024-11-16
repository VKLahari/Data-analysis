# Data-analysis
This is a part of my virtual case experience on pwc call centre trends analysis offered by forage. Here I used some useful insights like - total call answered/rejected, calls duration, calls resolved/unresolved, agents statistics, customer satisfaction, used slicers, cards, charts and used data cleansing, Dax function, added new measures & columns.
atrributes-
Call Id
Agent
Date
Time
Topic
Answered (Y/N)
Resolved
Speed of answer in seconds
Avg Talk Duration
Satisfaction rating

Here are the formulae I used for call centre trend analysis:
Answered = Calculate(Count(Sheet1[Call Id]),FILTER(Sheet1,Sheet1[Answered (Y/N)]= "Y"))
Resolved(Y) = CALCULATE(COUNT(Sheet1[Call Id]),FILTER(Sheet1,Sheet1[Resolved]="Y"))

This is a part of my virtual case experience on pwc contention retention offered by forage. Here I used some useful insights like - 
Churn rate versus network service type/contract type/paperless billing ,Created a dashboard using the defined KPIs to reflect customer demographics and insights.

Here are the formulae I used for retention(for calculating and analysis churn rate.):

% of Dependents = DIVIDE(CALCULATE(Count(Churn[Dependents]),Churn[Dependents]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[Dependents]),Churn[Churn]="Yes"),0)
% of Device Protection = DIVIDE(CALCULATE(COUNT(Churn[DeviceProtection]),Churn[DeviceProtection]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[DeviceProtection]),Churn[Churn]="Yes"),0)
% of No = DIVIDE(CALCULATE(COUNT(Churn[MultipleLines]),Churn[MultipleLines]="No",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[MultipleLines]),Churn[Churn]="Yes",Churn[MultipleLines] <> "No phone service"),0)
% of Online Backup = DIVIDE(CALCULATE(COUNT(Churn[OnlineBackup]),Churn[OnlineBackup]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[OnlineBackup]),Churn[Churn]="Yes"),0)
% of Online Security = DIVIDE(CALCULATE(COUNT(Churn[OnlineSecurity]),Churn[OnlineSecurity]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[OnlineSecurity]),Churn[Churn]="Yes"),0)
% of partner = DIVIDE(CALCULATE(COUNT(Churn[Partner]),Churn[Partner]="Yes",Churn[Churn]="Yes"),Calculate(COUNT(Churn[Partner]),Churn[Churn]="Yes"),0)
% of PhoneService = DIVIDE(CALCULATE(COUNT(Churn[PhoneService]),Churn[PhoneService]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[PhoneService]),Churn[Churn]="Yes"),0)
% of senior citizens = DIVIDE(CALCULATE(COUNT(Churn[SeniorCitizen]),Churn[SeniorCitizen]=1,Churn[Churn]="Yes"),CALCULATE(Count(Churn[SeniorCitizen]),Churn[Churn]="Yes"),0)
% of Streaming Movies = DIVIDE(CALCULATE(COUNT(Churn[StreamingMovies]),Churn[StreamingMovies]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[StreamingMovies]),Churn[Churn]="Yes"),0)
% of Streaming TV = DIVIDE(CALCULATE(COUNT(Churn[StreamingTV]),Churn[StreamingTV]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[StreamingTV]),Churn[Churn]="Yes"),0)
% of TechSupport = DIVIDE(CALCULATE(COUNT(Churn[TechSupport]),Churn[TechSupport]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[TechSupport]),Churn[Churn]="Yes"),0)
% of Yes = DIVIDE(CALCULATE(COUNT(Churn[MultipleLines]),Churn[MultipleLines]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[MultipleLines]),Churn[Churn]="Yes",Churn[MultipleLines] <> "No phone service"),0)
Churn Rate % = DIVIDE(CALCULATE(COUNT(Churn[Churn]),Churn[Churn]="Yes"),COUNT(Churn[Churn]),0)

