---
icon: git-merge
order: 101
---
# What is Process Mining?
![](/introduction/what-is-pm.png)
Process mining is a family of techniques used to analyze operational processes derived from event logs. Event logs can be found in many different types of information systems, from enterprise resource planning (ERP) systems (e.g., SAP) to case management platforms like Microsoft Dynamics. Event logs can also be found in IoT or embedded systems in industrial/manufacturing settings. The term event log is often synonymous with the more familiar term “audit logs”.  

Event logs consist of digital footprints or activities taken throughout the lifecycle of a case. For example, when you apply for a passport, you submit an application with your photos, references, payment and other forms. As your application is processed, events are recorded in a system. One officer might verify your references while another may print the actual passport, and a third packages it for delivery to your home address. Each of these activities (i.e. events) are recorded in a system until the passport application is completed. We can extract these events in the form of an event log, that allows us to view the process, its performance and any bottlenecks with process mining tools.

The three most common types of process mining are: 

_Process discovery_: In process discovery, we seek to uncover a process model based on event log data. Process discovery not only allows us to uncover the true sequence of events taking place in a process, but also highlights the varied paths taken to accomplish the same outcome. For example, in some less structured processes, staff may take slightly different steps in how they accomplish their work, despite arriving at the same result; these are known as process variants. Through process discovery we can visualize these process variants, identify bottlenecks, and identify the “happy path” - i.e., the path most instances of a process take or should take to be most efficient. This can help towards process standardization and lead to more consistent execution.

_Conformance checking_: In conformance checking, we build on process discovery to check whether a discovered process model fits the idealized (i.e. authoritative) process model. Often, we find that what happens in reality does not fit the idealized process model. When a process variant is not executing according to the desired model or service level standard, we have discovered a deviation. Conformance checking can also identify violations in a process such as the four eyes principle, for example, where two distinct approvers are necessary in a transaction to avoid fraud.  
 
Conformance checking has two additional applications relevant to service delivery in Government. First, one can compare a discovered process model with the directives, standards and policies that must be adhered to remain compliant. Secondly, we can check to determine whether processes are adhering to their service level agreements (SLA). This is important for revenue collection as the GC modernizes its fee structures and establishes SLAs. Programs working on a cost-recovery basis must ensure their SLA is. When SLAs are not adhered to, the GC is usually required to reimburse (i.e. remit) this fee, and therefore loses the revenue. 

_Enhancement_: In process enhancement we take our findings from both process discovery and conformance checking to implement improvements to a process. Such improvements are then monitored and adjusted in an iterative cycle until a process is optimized or considered “lean enough” that any further enhancements would yield diminishing returns. 

Process Mining data can be examined from multiple perspectives. The control-flow perspective of process mining pertains to the sequence and ordering of events in the form of a process model. The organizational perspective examines the different roles which stakeholders or actors play in a process, and their degree of involvement in a process; the organizational perspective can be visualized in the form of a social network diagram.  

