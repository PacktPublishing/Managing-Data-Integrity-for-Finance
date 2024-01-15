# Managing Data Integrity for Finance

<a href="https://www.packtpub.com/product/managing-data-integrity-for-finance/9781837630141"><img src="https://content.packt.com/B19758/cover_image_small.jpg" alt="Book Name" height="120px" align="left" style="margin: 0px 15px; border-color: white; border-style: solid; border-width: 1px;"></a>

**Chapter 10: Using Artificial Intelligence for Finance Data Quality Management** <br />
This chapter exposes you to artificial intelligence solutions relevant to data quality and data integrity management.

<br />
<br />
<br />
<br />
<br />

## Links and Files

#### ChatGPT
- https://chat.openai.com/auth/login
- https://chat.openai.com/g/g-HMNcP6w7d-data-analysis

#### Files for hands-on exercises
- [2020_Transactions.xlsx](https://github.com/PacktPublishing/Managing-Data-Integrity-for-Finance/blob/main/ch10/2020_Transactions.xlsx)
- [2022 Transactions.xlsx](https://github.com/PacktPublishing/Managing-Data-Integrity-for-Finance/blob/main/ch10/2022%20Transactions.xlsx)
- [NSW_Post_Code.xlsx](https://github.com/PacktPublishing/Managing-Data-Integrity-for-Finance/blob/main/ch10/NSW_Post_Code.xlsx)
- [Products.xlsx](https://github.com/PacktPublishing/Managing-Data-Integrity-for-Finance/blob/main/ch10/Products.xlsx)
- [Sales Price.xlsx](https://github.com/PacktPublishing/Managing-Data-Integrity-for-Finance/blob/main/ch10/Sales%20Price.xlsx)
- [Sales_Transactions.xlsx](https://github.com/PacktPublishing/Managing-Data-Integrity-for-Finance/blob/main/ch10/Sales_Transactions.xlsx)
#### Further reading
- https://www.mckinsey.com/capabilities/mckinsey-digital/our-insights/the-economic-potential-of-generative-ai-the-next-productivity-frontier
- https://www.gartner.com/en/topics/generative-ai
- https://365datascience.com/trending/chatgpt-code-interpreter-what-it-is-and-how-it-works/
- https://www.forbes.com/sites/bernardmarr/2023/02/07/will-chatgpt-put-data-analysts-out-of-work/?sh=250f2e254030
- https://www.forbes.com/sites/jackmccullough/2023/08/21/embracing-generative-ai-opportunities-and-risks-for-cfos/?sh=2fffb5c257f7
- https://openai.com/blog/introducing-gpts
- https://help.openai.com/en/articles/8555545-file-uploads-with-gpts-and-advanceddata-analysis-in-chatgpt
- https://www.bcg.com/publications/2023/generative-ai-in-finance-and-accounting
<br />

## Versions of the tools used
- A **ChatGPT Plus** account
- **Microsoft Excel** `2016` version or later

## Code blocks specific to the chapter
#### How we can use ChatGPT for data integrity
```
Search the internet and answer how can I use ChatGPT for data integrity?
```

#### Detecting anomalies in financial transaction data (first hands-on exercise)
<pre>
Please examine the contents of these two files and provide information as to their data structure and type of data that they contain.

Please validate the <b>Suburb</b> column in the Sales_Transactions.xlsx file to the NSW_Post_Code.xlsx file. Please identify any suburbs that have mismatches using this column between the two files.

For these mismatched suburbs, find the closest match based on the NSW Post Code.xlsx file based on similarity of spelling. Please list them in a table format for review prior to any updates.

Please update the <b>mismatched suburbs</b> in the Sales_Transactions.xlsx file based on the <b>closest match</b>. Kindly show the transactions in table format when completed.

Please export the updated <b>Sales_Transactions.xlsx</b> file reflecting the changes made.

</pre>

#### Detecting anomalies in financial transaction data (second hands-on exercise)
<pre>
Please analyze what this file contains and provide information as to the data structure and type of data it has.

Give me a preview of the data in the file.

Please provide the basic statistics such as the number of transactions in the file, as well as the number of <b>unique</b> and <b>distinct</b> transactions for each column.

Please check the <b>Transaction ID</b> column and identify if there are any transactions that are repeated.

Can you show the duplicate rows in the dataset?

Please remove the <b>duplicate</b> rows identified then provide the total distinct and unique transactions for the <b>Transaction ID</b> column.

Please provide the details of the transaction or transactions which do not have a date in the year <b>2020</b>.

Please update the year to <b>2020</b> for the Transaction Date and show the updated fields for this transaction.

Review the <b>Product_ID</b> and <b>Sales_Manager</b> columns to see if there are any unusual values.

Provide the details of the <b>top 10</b> transactions with the highest quantities.

For <b>Transaction ID 2020644</b>, update the Quantity to 200 and show the updated details.

Export the cleaned data to an Excel file.

Using the original dataset uploaded, create a <b>scatter chart</b> with sum of quantity on the Y-axis and the months on the X-axis.

Using the original dataset, create a <b>histogram</b> using the quantity column with bin size of 1,553.

Under which buckets do our values fall? Include the number of entries to understand the distribution.

Using the cleaned data, create a histogram with a bin size of 100 based on the <b>Quantity</b> column.

</pre>

#### Handling missing financial reporting data with AI (third hands-on exercise)
<pre>
Please examine the contents of these three files and provide information as to their data structure and the type of data that they contain.

For the 2022 Transactions.xlsx file, please check for possible duplicate transactions using the <b>Transaction Number</b>.

Can you check each of the columns in the 2022 Transactions.xlsx file for any <b>missing values</b>?

Can you please list the transactions with the missing values in table format?

Please calculate the Sales column by multiplying the <b>Quantity</b> column with the <b>Price</b> column. Update the data and list the transactions updated in table format.

Please check the <b>Quantity</b> column in the 2022 Transactions.xlsx file to see if there are any outliers.

Reviewing the <b>Quantity</b> column, please list in table format the top 20 transactions with the highest quantities.

I reviewed the invoice for <b>Transaction Number 22022110029</b>. The quantity should only be <b>120</b>. Please update it and show me the updated columns for this transaction.

Please review the <b>Currency</b> column and <b>Price</b> column in the <b>2022 Transactions.xlsx</b> file with the <b>Sales Price.xlsx</b> file. If there are inconsistencies, please list them in table format and add a column for the price difference.

Get the <b>Quantity</b> column for each of the transactions above and use this to calculate the total price difference. List them in a <b>table format</b> and include an overall total as well.

Calculate the total sales for <b>each Product key</b> in the 2022 Transactions.xlsx file and match it with the Products.xlsx file.

Can we make sure that all the products sold found in the <b>2022 Transactions.xlsx</b> file are in the <b>Products.xlsx</b> file?

Please update the Products.xlsx file with the details of the <b>Product Key 8</b> to <b>Calculator</b>.

Please export the <b>updated</b> 2022 Transactions.xlsx file which reflects the changes we have made.

</pre>
