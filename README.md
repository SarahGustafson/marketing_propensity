# Introduction
This project explores several classification techniques as applied to a bank's marketing campaign data.  The classification goal is to predict whether the client will subscribe a term deposit (variable y). 
<br> Source: https://archive.ics.uci.edu/ml/datasets/bank+marketing <br> <br>
It's recommended that the viewer read the Jupyter Notebook in NBViewer: https://nbviewer.jupyter.org/github/sgus1318/marketing_propensity/blob/master/Bank_DirectMarketing_Propensity.ipynb
<br><br>
# Data Dictionary:
#### Bank client data:
1 - age (numeric) <br>
2 - job : type of job (categorical: 'admin.', 'blue-collar', 'entrepreneur', 'housemaid', 'management', 'retired', 'self-employed', 'services', 'student', 'technician', 'unemployed', 'unknown') <br>
3 - marital : marital status (categorical: 'divorced', 'married', 'single', 'unknown'; note: 'divorced' means divorced or widowed) <br>
4 - education (categorical: 'basic.4y', 'basic.6y', 'basic.9y', 'high.school', 'illiterate', 'professional.course', 'university.degree', 'unknown') <br>
5 - default: has credit in default? (categorical: 'no','yes','unknown') <br>
6 - housing: has housing loan? (categorical: 'no','yes','unknown') <br>
7 - loan: has personal loan? (categorical: 'no','yes','unknown') <br>
#### Campaign Data:
8 - contact: contact communication type (categorical: 'cellular','telephone')  <br>
9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec') <br>
10 - day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri') <br>
11 - duration: last contact duration, in seconds (numeric). *IMPORTANT NOTE: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.*  <br>
#### Other:
12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)  <br>
13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted) <br>
14 - previous: number of contacts performed before this campaign and for this client (numeric)  <br>
15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')  <br>
#### Macroeconomic variables:
16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)  <br>
17 - cons.price.idx: consumer price index - monthly indicator (numeric)  <br>
18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric)  <br>
19 - euribor3m: euribor 3 month rate - daily indicator (numeric) <br>
20 - nr.employed: number of employees - quarterly indicator (numeric) <br>
#### Created Variables: <br>
21 - prev_campaign_contact - whether or not an individual was contacted during a previous marketing campaign <br>
22 - prev_call - whether or no an individual was contacted already during this campaign <br>
23 - white collar - whether an individual's occupation falls into the category 'entrepreneaur, management, or admin" <br>
24 - age_sq - individual's age squared <br>
25 - age_sqrt - square root of the individual's age <br>
26 - age_ln - the natural log of the individual's age <br>
27 - age_sq - individual's age squared <br>
28 - emp.var.rate_sq - employment variation rate squared <br>
29 - emp.var.rate_sqroot - square root of employment variation rate  <br>
30 - emp.var.rate_recip - reciprocal of employment variation rate  <br>
31 - emp.var.rate_ln - natural log of employment variation rate  <br>
32 - cons.price.idx_sq - consumer price index squared <br>
33 - cons.price.idx_sqroot - square root of consumer price index <br>
34 - cons.price.idx_recip - reciprocal of consumer price index <br>
35 - cons.price.idx_ln - natural log of consumer price index <br>
36 - cons.conf.idx_sq - consumer confidence index squared <br>
37 - cons.conf.idx_sqroot - square root of consumer confidence index <br>
38 - cons.conf.idx_recip - reciprocal of consumer confidence index <br>
39 - cons.conf.idx_ln - natural log of consumer confidence index <br>
40 - euribor3m_sq - euribor 3 month rate squared <br>
41 - euribor3m_sqroot - square root of euribor 3 month rate <br>
42 - euribor3m_recip - reciprocal of euribor 3 month rate <br>
43 - euribor3m_ln - natural log of euribor 3 month rate <br>
44 - nr.employed_sq - number of employees squared <br>
45 - nr.employed_sqroot - square root of number of employees <br>
46 - nr.employed_recip - reciprocal of number of employees <br>
47 - nr.employed_ln - natural log of number of employees <br>

#### Output variable (target):
Made_Deposit - has the client subscribed a term deposit? (binary: 1:yes, 0:no) <br>
