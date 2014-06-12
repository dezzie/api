---
layout: default
title: API Basics
nav: basics
---

### API basics

HMDA is a GET API that lives at ```https://api.consumerfinance.gov/data/hmda```.

- You can query the entire **dataset**.
- You can query **slices**, which are pre-loaded views of data we think are interesting.
- You can query **concepts**, which describe types of information found in the dataset.

##### Datasets
The endpoint for querying all data begins with ```/data/```.  

<a href="console/#!/data/getDataset_get_1" class="action-arrow"> Try it out <i class="icon-right"> </i></a>


| Endpoint | What it does |
| ------------- | -------------|
| ```/data/{dataset-name}``` | Gives all information about a dataset 
| [```/data/hmda```](https://api.consumerfinance.gov/data/hmda) | Gives mortgage lending data from 2007-2012.


##### Slices
The endpoint for slices goes looks like ```/data/hmda/{slice-name}```. 

<a href="console/#!/hmda/querySliceHmda_get_2" class="action-arrow"> See the current slices <i class="icon-right"> </i></a>


| Endpoint | What it does |
| ------------- | -------------|
| [```/data/hmda/{slice-name}```](https://api.consumerfinance.gov/data/hmda/slice) | Gives information about a concept and describes its possible valaues
| [```/data/hmda/{slice-name.extension}```](https://api.consumerfinance.gov/data/hmda/concept/as_of_year.json) | Gives you the information in JSON, JSONP, XML, HTML, or CSV.

##### Concepts
The endpoint for querying concepts is ```/data/hmda/{concept-name}```.  

<a href="console/#!/hmda/getConceptHmda_get_1" class="action-arrow"> See the list of all concepts <i class="icon-right"> </i></a>

| Endpoint | What it does |
| ------------- | -------------|
| [```/data/hmda/{concept-name}```](https://api.consumerfinance.gov/data/hmda/slice/application_groups) | Defines a type of information in the dataset and its possible values.
| [```/data/hmda/{concept-name.extension}```](https://api.consumerfinance.gov/data/hmda/slice/application_groups.json) | Gives you the information in JSON, JSONP, XML, HTML, or CSV.
| [```/data/hmda/{slice-name}/{concept-name}```](https://api.consumerfinance.gov/data/hmda/slice/application_groups.json) | If querying both slices and concepts, call slices first, then concepts.

### Putting it all together
Use [API calls](console/) to generate the request URLs for specific pieces of information, and try out these examples:

##### How many people have bought a house in your neighborhood?
Fill in your [state](https://api.consumerfinance.gov/data/hmda/concept/state_code) and [census tract](https://ask.census.gov/faq.php?id=5000&amp;faqId=127):
&#x20;<pre>https://api.consumerfinance.gov/data/hmda/slice/hmda_lar.json?#!/as_of_year=2012&amp;state_code-1={YOUR STATE CODE}&amp;census_tract_number-1={YOUR CENSUS TRACT}&amp;property_type=1,2&amp;owner_occupancy=1&amp;action_taken=1&amp;loan_purpose=1&amp;lien_status=1</pre>

##### The most common loan denial reason for people like you
Try using your [metro area](https://api.consumerfinance.gov/data/hmda/concept/msamd) and demographics like [sex](https://api.consumerfinance.gov:443/data/hmda/concept/sex), [race](https://api.consumerfinance.gov:443/data/hmda/concept/race), [ethnicity](https://api.consumerfinance.gov:443/data/hmda/concept/ethnicity), or income range.

&#x20;<pre>https://api.consumerfinance.gov/data/hmda/slice/hmda_lar.json?#!/as_of_year=2012&amp;msamd-1={YOUR METRO AREA}&amp;property_type=1&amp;owner_occupancy=1&amp;loan_purpose=1&amp;lien_status=1&amp;applicant_sex={SEX}&amp;applicant_race_1={RACE}&amp;applicant_ethnicity={ETHNICITY}&amp;applicant_income_000s-min&gt;{MIN INCOME}&amp;applicant_income_000s-max&lt;{MAX INCOME}&amp;select=denial_reason_name_1,count&amp;section=summary</pre>

##### Change in number of new homebuyers in DC from 2010-2012
<pre>https://api.consumerfinance.gov/data/hmda/slice/hmda_lar.json?#!/as_of_year=2012,2011,2010&amp;state_code=11&amp;property_type=1,2&amp;owner_occupancy=1&amp;lien_status=1&amp;action_taken=1&amp;select=state_name,county_name,as_of_year,count</pre>
&#x20;<a href="https://api.consumerfinance.gov/data/hmda/slice/hmda_lar.json?#!/as_of_year=2012,2011,2010&amp;state_code=11&amp;property_type=1,2&amp;owner_occupancy=1&amp;lien_status=1&amp;action_taken=1&amp;select=state_name,county_name,as_of_year,count&amp;" class="action-arrow">Call it <i class="icon-right"> </i></a> or <a href="http://www.consumerfinance.gov/hmda/explore#!/as_of_year=2012,2011,2010&amp;state_code=11&amp;property_type=1,2&amp;owner_occupancy=1&amp;lien_status=1&amp;action_taken=1&amp;select=state_name,county_name,as_of_year,count&amp;" class="action-arrow">Preview the data<i class="icon-right"> </i></a>

##### Compare refinances and home purchases in 2012 across America
&#x20;<pre>https://api.consumerfinance.gov/data/hmda/slice/hmda_lar.xml?#!/property_type=1,2&amp;action_taken=1&amp;select=as_of_year,loan_purpose_name,count&amp;section=summary</pre>
&#x20;<a class="action-arrow" href="https://api.consumerfinance.gov/data/hmda/slice/hmda_lar.xml?#!/property_type=1,2&amp;action_taken=1&amp;select=as_of_year,loan_purpose_name,count&amp;section=summary">Call it <i class="icon-right"> </i></a> or <a class="action-arrow" href="http://www.consumerfinance.gov/hmda/explore.html#!/property_type=1,2&amp;action_taken=1&amp;select=as_of_year,loan_purpose_name,count&amp;section=summary">Preview the data <i class="icon-right"> </i></a>

### Previewing your query in plain language using HMDA Explore
If assessing your results in machine format is unsuable to you, you can preview your data in neat and tidy tables using our [HMDA Explore](http://consumerfinance.gov/hmda/explore) tool. Substitute the machine part of the API's URL with that of the front-facing tool.

##### Replace this
```https://api.consumerfinance.gov/data/hmda/slice/hmda_lar.xml?#/{all your other parameters}```

##### With this
```http://www.consumerfinance.gov/hmda/explore.html#!/{all your other parameters}```

<body id="basics"></body>