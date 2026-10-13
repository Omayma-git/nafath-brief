Version: NAFATH-V2
Track:  Networking 

## Overview
A telecom operator is launching a 5G service for emergency responders who need reliable communication during critical situations. Six IT fields work together to improve service availability during congestion, outages, and cyber attacks. Software can handle failed requests through carefully designed retry mechanisms. AI can help predict network performance problems using traffic data. Mobile applications can store essential information offline and synchronize it when connectivity returns. Networking can use dedicated 5G network slices and appropriate quality-of-service policies to support emergency communications. Cybersecurity helps detect attacks, respond to incidents, and restore affected services. Data systems can organize service usage reports across regions to support monitoring and decision-making. Together, these fields help the operator design a more resilient emergency communication service.

## Software
GET, HEAD, OPTIONS, and TRACE are safe methods. They are designed to obtain information without requesting changes to the server's state. These safe methods are also idempotent, along with PUT and DELETE, because repeating the same request has the same intended effect as sending it once. This matters when a connection fails: clients can retry idempotent requests without duplicating the intended action, while retrying POST may cause unintended duplicate operations.
Resource: RFC 9110 - HTTP Semantics - https://www.rfc-editor.org/rfc/rfc9110.html

## AI
Overfitting happens when an AI model learns the training data too closely, including patterns that may not appear in new data. For a telecom operator, this could mean predicting congestion accurately during training but performing poorly on new network traffic. Cross-validation helps detect this problem by training and evaluating the model on different data subsets. Consistently poor validation results compared with training performance can indicate overfitting.
Resource: Scikit-learn - Cross-validation: evaluating estimator performance - https://scikit-learn.org/stable/modules/cross_validation.html

## Mobile
When offline, the responder's mobile app should keep essential information accessible and save new updates locally to prevent data loss. It should clearly show the connection status and warn users when urgent reports have not been delivered. Once connectivity returns, the app should synchronize queued changes with the server, retry failed transfers carefully, and resolve any conflicts between local and server data. This helps responders continue working while keeping their information consistent.
Resource: Android Developers - Build an offline-first app - https://developer.android.com/topic/architecture/data-layer/offline-first

## Networking
5G network slicing allows operators to create logical network slices with connectivity tailored to different services. In an emergency communication system, a slice could be configured to prioritize responders' traffic and provide suitable quality of service during network congestion. This can help emergency teams maintain more reliable communication when many people are using the network. However, network slicing alone cannot guarantee service during a complete network outage, so additional resilience measures are still needed.
Resource: GSMA - 5G Standalone opens up new opportunities - https://www.gsma.com/solutions-and-impact/technologies/networks/gsma_resources/5g-standalone-opens-up-new-opportunities/

## Cybersecurity
NIST's incident response model includes six functions: Govern, Identify, Protect, Detect, Respond, and Recover. The first three support preparation, while the last three focus on handling incidents. During a cyberattack on emergency communications, the operator should detect suspicious activity, investigate the incident, contain affected systems, and communicate with relevant teams. Recovery involves restoring services safely and checking that systems operate correctly. Lessons learned should improve future protection and response plans.
Resource: NIST - Incident Response Recommendations and Considerations for Cybersecurity Risk Management - https://doi.org/10.6028/NIST.SP.800-61r3

## Data
A star schema uses a central fact table connected to dimension tables, while a snowflake schema normalizes dimensions into multiple related tables. For daily network usage reports by region, a star schema is generally more suitable because it simplifies reporting and analysis. The fact table could store daily data usage and connection counts, while date and region dimensions support filtering and comparisons. A snowflake schema may reduce duplicated dimension data but introduces more relationships and complexity.
Resource: Microsoft Learn - Understand star schema and the importance for Power BI - https://learn.microsoft.com/en-us/power-bi/guidance/star-schema

## Misconception in My Track

## Open Question
