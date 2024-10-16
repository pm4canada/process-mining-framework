---
icon: stack
---
# Data Preparation

## Minimum Data Requirements
Process mining uses digital footprints inside existing information systems to generate what are known as event logs. An event log is a collection of events of different cases, with timestamps and activities. **Three columns are needed at a minimum for process mining: case_id, event, and timestamp.**

The key requirement to producing an event log is that actions are recorded in information systems. Systems that record event log data are known as process aware information systems (PAIS) (Dumas et al., 2005). Examples of PAIS include ERP systems (Oracle, SAP), CRM systems (Salesforce, Microsoft Dynamics) and intelligent business process management suites (Appian, IBM, Pegasystems). 

**An example event log looks similar to this table below:**

| case_id 	| event           	    | timestamp  | purchaser | 
| --------- | --------------------- | ---------- | --------- | 
| 121     	| purchaseOrderCreated	| 31/12/2020 11:59   | Bob 	|
| 121     	| purchaseOrderApproved	| 05/01/2021 13:53   | Bob 	|
| 121     	| purchasePaid | 01/02/2021 14:55   | Bob 	|
| 122     	| purchaseOrderCreated	| 05/01/2021 12:55   | Jane 	|
| 122     	| purchaseOrderApproved	| 10/01/2021 09:30   | Jane 	|
| 122     	| purchasePaid | 28/01/2021 15:33   | Jane 	|
| 123     	| purchaseOrderCreated	| 10/04/2021 23:59   | John 	|
| 123     	| purchaseOrderApproved	| 24/04/2021 23:59   | John 	|
| 123     	| purchasePaid | 04/05/2021 23:59   | John 	|
| 124     	| purchaseOrderCreated	|  12/01/2021 15:22 | Jill 	|
| 124     	| purchaseOrderApproved	| 12/15/2021 16:49   | Jill 	|
| 124     	| purchasePaid | 05/01/2022 13:00   | Jill 	|

Event logs are typically stored in CSV or XLSX format. There are more sophisticated formats such as XES which allow for advanced process mining techniques. Sample (open data) event logs for process mining can be found below:
[!file icon="log" text="IEEE Task Force on Process Mining - Event Logs"](https://www.tf-pm.org/resources/logs)

## Negotiating Access to Data
Obtaining access to data is one of the hardest parts of process mining. People who are new to Process Mining may not fully understand it, or fear that it may expose issues within their business that are not well perceived. In a Government context where anything can be publicly scrutanized (e.g. ATIP), this is especially true. To help teams obtain management consent to access process mining data, we've prepared a briefing note template to help accelerate the process. 

[!file icon="file" text="Sample Briefing Note (DOCX)"](/framework/data-access-process-mining-briefing-note.docx)

## Data Extraction & Cleaning
Data extraction and cleaning is by far the longest part of a process mining project. As we mentioned above, data quality differs, depending on the source system. There are two ways to extract data into an event-log format:
1.	Using plug-ins (aka connectors) provided process mining tools to connect directly to source systems.
2.	Manual data extraction via a database or API export.

If you’re lucky enough to be working with a source system and process mining tool that has a ready-made connector, then option #1 is surely the best way forward and will accelerate time to value. However, in many cases, option #2 will prevail. Most PM projects we’ve undertaken in the GC (so far) used option #2 as it was rare for us to get permission to connect directly to source systems without an intermediary who would filter data exports to ensure no confidential or personal information was shared. Likewise, often selective exports of data are stored in data lakes/warehouses, which 

[!ref target="blank" icon="mark-github" text="logprep4pm: Log Filtering and Preprocessing Library for Process Mining"](https://github.com/ProcessMining-uOttawa/logprep4pm)

When engaging in option 2, we’ve made heavy use of Python, the popular Pandas library and the logprep4pm module developed in collaboration with the University of Ottawa. This approach has several benefits: 
-	The use of Jupyter notebooks and Pandas allows you to document the steps taken to clean your dataset and transform it into event log format. This enhances reproducibility. 
-	The notebook can be easily turned into a Python script for continuously updating new data into a process mining tool.
