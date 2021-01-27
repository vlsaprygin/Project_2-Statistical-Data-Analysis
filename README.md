## Project description

You work as an analyst for the telecom operator Megaline. The company offers its clients two prepaid plans, Surf and Ultimate.<br>
The commercial department wants to know which of the plans brings in more revenue in order to adjust the advertising budget.<br>
You are going to carry out a preliminary analysis of the plans based on a relatively small client selection.<br>
You'll have the data on 500 Megaline clients: who the clients are, where they're from, which plan they use, and the number of calls they made and text messages they sent in 2018.<br>
Your job is to analyze clients' behavior and determine which prepaid plan brings in more revenue.


## Description of the plans

`Megaline rounds seconds up to minutes, and megabytes to gigabytes. For calls, each individual call is rounded up: even if the call lasted just one second,
it will be counted as one minute. For web traffic, individual web sessions are not rounded up.<br> Instead, the total for the month is rounded up.<br>
If someone uses 1025 megabytes this month, they will be charged for 2 gigabytes.`

#### `Surf` <br>

* Monthly charge: $20<br>
* 500 monthly minutes, 50 texts, and 15 GB of data<br>

`After exceeding the package limits:`<br>
* 1 minute: 3 cents<br>
* 1 text message: 3 cents<br>
* 1 GB of data: $10<br>

#### `Ultimate`
* Monthly charge: $70<br>
* 3000 monthly minutes, 1000 text messages, and 30 GB of data<br>

`After exceeding the package limits:`<br>
* 1 minute: 1 cent<br>
* 1 text message: 1 cent<br>
* 1 GB of data: $7<br>

## Instructions on completing the project


### `Step 1. Open the data file and study the general information`

File path:<br>
/datasets/megaline_calls.csv Download dataset<br>
/datasets/megaline_internet.csv Download dataset<br>
/datasets/megaline_messages.csv Download dataset<br>
/datasets/megaline_plans.csv Download dataset<br>
/datasets/megaline_users.csv Download dataset<br>

### `Step 2. Prepare the data`

* Convert the data to the necessary types<br>
* Find and eliminate errors in the data<br>
* Explain what errors you found and how you removed them.<br>

`Note: many calls have a duration of 0.0 minutes. These might be missed calls. Whether or not to preprocess these values is up to you; assess how much their absence would affect the results of your analysis.`

### `For each user, find:`

* The number of calls made and minutes used per month
* The number of text messages sent per month
* The volume of data per month
* The monthly revenue from each user (subtract the free package limit from the total number of calls, text messages, and data; multiply the result by the calling plan value; add the monthly charge depending on the calling plan)

### `Step 3. Analyze the data`

* Describe the customers' behavior.<br>
* Find the minutes, texts, and volume of data the users of each plan require per month.<br>
* Calculate the mean, dispersion, and standard deviation.<br>
* Plot histograms. Describe the distributions.

### `Step 4. Test the hypotheses`

* The average revenue from users of Ultimate and Surf calling plans differs.<br>
* The average revenue from users in NY-NJ area is different from that of the users from other regions.<br>
* You decide what alpha value to use.

### `Explain:`

* How you formulated the null and alternative hypotheses.
* What criterion you used to test the hypotheses and why.

### `Step 5. Write an overall conclusion`

`Format: Complete the task in Jupyter Notebook. Put the programming code in code cells and text explanations in markdown cells, then apply formatting and headings.`<br>

`Description of the data
Remember! Megaline rounds seconds up to minutes, and megabytes to gigabytes. For calls, each individual call is rounded up: even if the call lasted just one second, it will be counted as one minute. For web traffic, individual web sessions are not rounded up. Instead, the total for the month is rounded up. If someone uses 1025 megabytes this month, they will be charged for 2 gigabytes.`


### `The users table (data on users):`

* user_id — unique user identifier<br>
* first_name — user's name<br>
* last_name — user's last name<br>
* age — user's age (years)<br>
* reg_date — subscription date (dd, mm, yy)<br>
* churn_date — the date the user stopped using the service (if the value is missing, the calling plan was being used when this data was retrieved)<br>
* city — user's city of residence<br>
* plan — calling plan name<br>

### `The calls table (data on calls):`

* id — unique call identifier<br>
* call_date — call date<br>
* duration — call duration (in minutes)<br>
* user_id — the identifier of the user making the call<br>

### `The messages table (data on texts):`

* id — unique text message identifier<br>
* message_date — text message date<br>
* user_id — the identifier of the user sending the text<br>

### `The internet table (data on web sessions):`

* id — unique session identifier<br>
* mb_used — the volume of data spent during the session (in megabytes)<br>
* session_date — web session date<br>
* user_id — user identifier<br>

### `The plans table (data on the plans):`

* plan_name — calling plan name<br>
* usd_monthly_fee — monthly charge in US dollars<br>
* minutes_included — monthly minute allowance<br>
* messages_included — monthly text allowance<br>
* mb_per_month_included — data volume allowance (in megabytes)<br>
* usd_per_minute — price per minute after exceeding the package limits (e.g., if the package includes 100 minutes, the 101st minute will be charged)<br>
* usd_per_message — price per text after exceeding the package limits<br>
* usd_per_gb — price per extra gigabyte of data after exceeding the package limits (1 GB = 1024 megabytes)
