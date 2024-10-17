---
icon: codescan-checkmark
order: 101
---
# Process Mining & Analysis
The fun part of process mining is the analysis that comes from good, clean and representative data. Process Mining is an interative process. As you prepare your event log, you will go through multiple iterations of data cleansing until you're satisfied that the process model discovered in your process mining software represents the true process model. This is why we recommend the use of Jupyter Notebooks in conjunction with the [logprep4pm](https://github.com/ProcessMining-uOttawa/logprep4pm) Python module previously mentioned. This approach allows you to document the steps you've taken to prepare your dataset for process mining. It will come in handy in the future as you may forget what steps you took and why.

Once your dataset is ready, it's time to perform analysis. Make sure to validate your process model with the process owner as they may highlight any gaps or inaccuracies that might need reivision. Go back to the research questions you initially proposed and see if you can answer them with the generated process model. You may also discover new findings (after the fact) that weren't part of your original research questions. Some initial questions you might pose include:

1. What is the mean and median processing time for a case? Is this too long?
2. Where are the bottlenecks and are they major?
3. Is there a clear happy path illustrated in the process model or does it look like spaghetti?
4. Is there a lot of re-work?
5. Where are the quick wins that we can implement quickly?
6. If we reassign work to a different resource, would the processing time improve?

This list is not meant to be exhaustive. There are many dimensions to process analysis. We recommend looking at example case studies to help understand the possibilities and remedies.

## A Case Study in the Government of Canada
[![](/framework/publication.png)-](https://ruor.uottawa.ca/items/eb3902c2-7704-4cf6-92ec-110b2f669b5f)
To illustrate Process Mining in action within the Government of Canada, we have published a workshop paper at the [International Conference on Process Mining](https://icpmconference.org/). It outlines our methodology, findings and positive impacts on improving the digital service delivery of personnel security screening. The interventions applied within our case study not only helped reduce the time to process security clearances, but also accelerated hiring time as a result. Though this work was carried out in only one government department, it serves as a model for how other Government departments can improve their personnel security screening processs.

To better understand the analysis phase of our framework, we encourage you to [read this article](https://ruor.uottawa.ca/items/eb3902c2-7704-4cf6-92ec-110b2f669b5f). There are sample [Jupyter notebooks](https://github.com/ProcessMining-uOttawa/logprep4pm/blob/main/logprep4pm-example.ipynb) that illustrate how we cleaned our data, along with example process maps generated from our dataset. 


