<center> <img src="Website/images/news.svg" width="150" height="150"> </center>

# Understanding Financial Reports using Natural Language Processing

This project serves as my undergraduate Computer Science thesis in Natural Language Processing.

## Background

This project investigates how mutual funds leverage credit derivative by studying their routine filings to the U.S. Securities and Exchange Commission. Credit derivatives are used to transfer credit risk related to an underlying entity from one party to another without transferring the actual underlying entity.

Instead of studying all credit derivatives, we focus on Credit Default Swap (CDS), one of the popular credit derivatives that were considered the culprit of the 2007-2008 financial crisis. A credit default swap is a particular type of swap designed to transfer the credit exposure of fixed income products between two or more parties. In a credit default swap, the buyer of the swap makes payments to the swaps seller up until the maturity date of a contract. In return, the seller agrees that, in the event that the debt issuer defaults or experiences another credit event, the seller will pay the buyer the securitys premium as well as all interest payments that would have been paid between that time and the securitys maturity date.

CDS is traded over-the-counter, thus there exists little public information on its trading activities for the outside investors. However, such information is valuable. CDS is designed as a hedging tool that the buyers use to protect themselves from potential default events of the reference entity. Besides, it is also used for speculation and liquidity management especially during a crisis.

Before SEC has requested more frequent and detailed fund holdings reporting at the end of 2016, mutual funds filed the forms in discrepant formats. This made it extremely difficult to effectively extract information from the reports for carrying out further analysis. There exist some previous studies that explored how mutual funds have made use of CDS (Adam and Guttler, 2015, Jiang and Zhu, 2016), but only examined a fraction of institutions over a short period of time. In this project, we aim to extract as much CDS-related information as possible from all the filings available to date to enable more thorough downstream analysis. This information appears not only in the form of charts but also in words, thus Natural Language Processing (NLP) is the key.

## Tools Used

1. For tagging the entities in the reports, I developed a annotation tool which can be found here: `https://github.com/sudhamstarun/Text-Annotation-Tool`
2. The core of this project can be recognised as a Named Entity Recognition Task, so we implemented a BiLSTM-CRF model and a CRF model to conduct sequence labelling on unsturctured data. Its implementation is still in progress and can be found here: `https://github.com/sudhamstarun/AwesomeNER` <br>
3. A RESTful API based web application is developed to work as a Credit Default Swap Search Engine in order to make it extremely accessible for researchers and analysts to have access to all the historical mentions of Credit Default Swap by simply searching *counterparty* or *reference entities* `https://github.com/sudhamstarun/Credit-Default-Swap-Search-Engine`

## Authors:

[Tarun Sudhams](https://github.com/sudhamstarun)
[Varun Vamsi](https://github.com/Varunvamsi)
