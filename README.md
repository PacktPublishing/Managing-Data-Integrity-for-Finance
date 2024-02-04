# Managing Data Integrity for Finance

<a href="https://www.packtpub.com/product/managing-data-integrity-for-finance/9781837630141"><img src="https://content.packt.com/B19758/cover_image_small.jpg" alt="Managing Data Integrity for Finance" height="256px" align="right"></a>

This is the code repository for [Managing Data Integrity for Finance](https://www.packtpub.com/product/managing-data-integrity-for-finance/9781837630141), published by Packt. 

**Discover practical data quality management strategies for finance analysts and data professionals** <br />

## What is this book about?
Data integrity management plays a critical role in the success and effectiveness of organizations trying to use financial and operational data to make business decisions. Unfortunately, there is a big gap when it comes to the analysis and management of finance data along with the proper implementation of complex data systems across various organizations.

This book covers the following exciting features: 
* Develop a customized financial data quality scorecard
* Utilize business intelligence tools to detect, manage, and resolve data integrity issues
* Find out how to use managed cloud-based ledger databases for financial data integrity
* Apply database locking techniques to prevent transaction integrity issues involving finance data
* Discover the methods to detect fraudulent transactions affecting financial report integrity
* Use artificial intelligence-powered solutions to resolve various data integrity issues and challenges

If you feel this book is for you, get your [copy]([https://www.amazon.com/Managing-Data-Integrity-Finance-professionals/dp/1837630143](https://www.amazon.com/Managing-Data-Integrity-Finance-professionals-ebook/dp/B0CN7DGY92/)) today!


## Instructions and Navigations
All of the code is organized into folders.

The code will look like the following:
```
INSERT INTO Accounts (AccountID, Balance)
VALUES (1, 100.00);
```

When we wish to draw your attention to a particular part of a code block, the relevant lines or items are set in bold:
<pre>
CREATE TABLE Accounts (
    AccountID int,
    CustomerName varchar(100),
    <b>Balance decimal(10, 2) CHECK (Balance >= 0) </b>
);
</pre>

**Following is what you need for this book:**
This book is intended for financial analysts, technical leaders, and data analysts interested in learning practical strategies for managing data integrity and data quality using relevant solutions, tools, and strategies.

With the following software and hardware list you can run all code files present in the book (Chapter 1-10).

### Software and Hardware List
You are expected to have a basic understanding of concepts relating to finance, accounting, and data analysis. Basic knowledge of finance management is not required but will help with grasping the intermediate topics of the book.

| Software required                                                                    | OS required                        |
| -------------------------------------------------------------------------------------| -----------------------------------|
|    Microsoft Power BI Desktop                                                      | Windows (preferred) | 		
|   Tableau, Tableau Prep Builder, and Tableau Cloud                                 | Windows (preferred) | 		
|   Alteryx Designer                      			                       			          | Windows (preferred) | 		


### Related products <Other books you may enjoy>
* Driving Data Quality with Data Contracts  [[Packt]](https://www.packtpub.com/product/driving-data-quality-with-data-contracts/9781837635009) [[Amazon]](https://www.amazon.com/Driving-Data-Quality-Contracts-comprehensive/dp/1837635005/)
  
* Practical Data Quality  [[Packt]](https://www.packtpub.com/product/practical-data-quality/9781804610787) [[Amazon]](https://www.amazon.com/Practical-Data-Quality-real-world-organization/dp/180461078X)
  
## Get to Know the Author
**Jane Sarah Lat** is a finance professional with over 14 years of experience in financial management and analysis for multiple blue-chip multinational organizations. In addition to being a **Certified Management Accountant (CMA U.S.)** and having a **Graduate Diploma in Chartered Accounting (GradDipCA)**, she also holds various technical certifications, including Microsoft Certified Data Analyst Associate and Advanced Proficiency in KNIME Analytics Platform. Over the past few years, she has been sharing her experience and expertise at international conferences to discuss practical strategies on finance, data analysis, and management accounting. She is also the President of the **Institute of Management Accountants (IMA)** Australia and New Zealand chapter.

### Download a free PDF
<i>If you have already purchased the print or Kindle version of this book, you can get a DRM-free PDF version at no cost. Simply click on the link and fill out the form to claim your free PDF. </i>  [[Packt free PDF]](https://download.packt.com/free-ebook/9781837630141)
