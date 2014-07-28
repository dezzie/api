---
layout: default
title: Field Reference
nav: fields
---

### Field reference for HMDA LAR data

Why so many rows and fields? Don't be alarmed–there's a lot of information in HMDA LAR data. HMDA LAR data is mortgage data. LAR means loan application stuff only. It does not have data for people who are currently paying their mortgage.

But you can hook it up to other datasets. We ate our own dog food at cf.gov/hmda by hooking up census data, for example.

We didn't choose the names and we can't change them, so we think this table will help.

If you get serious about working with this data know what it can and can't say.


#### HMDA Loan Application Register fields
<div class="mobile-warning">

              <i class="icon-error-alt"></i> We recommend viewing this table in landscape mode on your mobile device.

            </div>

##### Location
| Endpoint | What it does |
| ------------- | -------------|
| ```/data/{dataset-name}``` | Gives all information about a dataset 
| [```/data/hmda```](https://api.consumerfinance.gov/data/hmda) | Gives mortgage lending data from 2007-2012.

##### Demographics
| Endpoint | What it does |
| ------------- | -------------|
| ```/data/{dataset-name}``` | Gives all information about a dataset 
| [```/data/hmda```](https://api.consumerfinance.gov/data/hmda) | Gives mortgage lending data from 2007-2012.

##### Loans
| Endpoint | What it does |
| ------------- | -------------|
| ```/data/{dataset-name}``` | Gives all information about a dataset 
| [```/data/hmda```](https://api.consumerfinance.gov/data/hmda) | Gives mortgage lending data from 2007-2012.

##### Lenders
| Endpoint | What it does |
| ------------- | -------------|
| ```/data/{dataset-name}``` | Gives all information about a dataset 
| [```/data/hmda```](https://api.consumerfinance.gov/data/hmda) | Gives mortgage lending data from 2007-2012.

##### Property
| Endpoint | What it does |
| ------------- | -------------|
| ```/data/{dataset-name}``` | Gives all information about a dataset 
| [```/data/hmda```](https://api.consumerfinance.gov/data/hmda) | Gives mortgage lending data from 2007-2012.

<div class="expandable expandable">
    <header class="expandable-header">
        <span class="expandable-text">Show</span><h4> the list of calls</h4><a class="expandable-button" href="#"> </a>
    </header>

<div class="expandable-content expandable-hidden" style="display:none;">

<table class="table-code">
<thead>
<tr>
<th>Operator</th>
<th>What it means</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>=</code></td>
<td>equality</td>
<td><code>name = "Phillip"</code></td>
</tr>
<tr>
<td><code>!=</code></td>
<td>inequality</td>
<td><code>state != "Alaska"</code></td>
</tr>
<tr>
<td><code>&gt;</code></td>
<td>greater than</td>
<td><code>age &gt; 18</code></td>
</tr>
<tr>
<td><code>&gt;=</code></td>
<td>greater than or equal</td>
<td><code>square_miles &gt;= 1000</code></td>
</tr>
<tr>
<td><code>&lt;</code></td>
<td>less than</td>
<td><code>age &lt; 65</code></td>
</tr>
<tr>
<td><code>&lt;=</code></td>
<td>less than or equal</td>
<td><code>square_miles &lt;= 1000</code></td>
</tr>
<tr>
<td><code>LIKE</code></td>
<td>matches strings</td>
<td><code>name LIKE "Pete%"</code> would match "Pete, "Peter," or anything that starts with "Pete"</td>
</tr>
<tr>
<td><code>ILIKE</code></td>
<td>matches case-insensitive strings</td>
<td><code>name ILIKE "%rick"</code> would match "Rick" as well as "Yorick," "Harrick," or anything else with "rick" in it</td>
</tr>
<tr>
<td><code>IS NULL</code></td>
<td>existence of a value</td>
<td><code>city is NULL</code></td>
</tr>
<tr>
<td><code>IS NOT NULL</code></td>
<td>non-existence of a value</td>
<td><code>city IS NOT NULL</code></td>
</tr>
</tbody>
</table>
    </div>
</div>


<div class="expandable expandable">
    <header class="expandable-header">
        <span class="expandable-text">Show</span><h4> the list of current slices</h4><a class="expandable-button" href="#"> </a>
    </header>

<div class="expandable-content expandable-hidden" style="display:none;">

<table class="table-code">
<thead>
<tr>
<th>Operator</th>
<th>What it means</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>AND</code></td>
<td>logical AND of two comparisons</td>
<td><code>state = "Alaska" AND age &gt; 18</code></td>
</tr>
<tr>
<td><code>OR</code></td>
<td>logical OR of two comparisons</td>
<td><code>state = "Alaksa" OR state = "Hawaii"</code></td>
</tr>
<tr>
<td><code>NOT</code></td>
<td>negation of a comparison</td>
<td><code>NOT (state = "Alaska" OR state = "Hawaii"</code></td>
</tr>
<tr>
<td><code>()</code></td>
<td>grouping or order of operations</td>
<td><code>(state = "Alaska" OR state = "Hawaii") AND age &gt; 18</code></td>
</tr>
</tbody>
</table>
    </div>
    </div><!-- /.expandable-content -->


<!--AUTO TABLE
<table id="hmda-lar-fields" class="field-table">
	<colgroup>
		<col span="1" style="width: 36%;">
		<col span="1" style="width: 31.6%;">
		<col span="1" style="width: 16.65%;">
		<col span="1" style="width: 15.75%;">
	</colgroup>
<thead>
<tr>
<th>Field name</th>
<th>Description</th>
<th>Data type</th>
<th>Indexed?</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
-->



<body id="fields">
</body>