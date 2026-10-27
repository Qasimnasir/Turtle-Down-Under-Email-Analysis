# Turtle-Down-Under-Email-Analysis
Python-based email analytics project for Turtle Down Under, analysing travel enquiries, agent behaviour, response times, conversation lifecycles, booking patterns and email classification using NLP and data visualisation.
# Email Enquiry and Travel Agent Behaviour Analysis

**Project:** Business Email Analytics and Operational Performance Assessment
**Organisation:** Turtle Down Under
**Prepared by:** Qasim Nasir

## 1. How many emails are exchanged within each enquiry?

**Objective:** To analyse the total number of email interactions associated with each enquiry, including initial requests, replies, forwarded messages and follow-up communications.

By tracking enquiry reference numbers and related email conversations, we can determine how frequently travel agents and internal staff communicate throughout an enquiry's lifecycle.

**Business Value:** This analysis will help identify highly engaged travel agents, measure communication frequency, and understand which enquiries require additional coordination. When combined with response-time metrics, it can also provide insights into communication efficiency and identify conversations involving repeated follow-ups or unnecessary delays.

## 2. Which enquiries are new, ongoing or closed?

**Objective:** To develop a structured enquiry classification system that automatically identifies the operational status of each enquiry based on email content, conversation history and business-specific indicators.

We can implement rule-based classification and prompt engineering techniques to distinguish between newly received enquiries, active discussions and completed or closed cases.

**Business Value:** This will enable the company to monitor enquiry progress, identify outstanding requests, prioritise follow-ups and reduce the risk of unresolved enquiries being overlooked. Clear classification criteria will also support more accurate reporting on enquiry completion and operational workload.

## 3. How quickly do internal staff and external travel agents respond to enquiries?

**Objective:** To measure communication response times between Turtle Down Under's operational staff and external travel agents throughout the enquiry process.

This analysis will calculate the time taken by internal staff to respond to incoming requests and the time taken by external agents to reply to quotations, requests for clarification and follow-up communications.

**Business Value:** By measuring response times separately for both parties, the company can identify communication delays, assess operational efficiency and determine whether outstanding enquiries are awaiting internal action or an external agent's response.

This will help identify opportunities to improve turnaround times and reduce unnecessary delays in the enquiry and booking process.

## 4. Which travel agents contact the company most frequently, and what services do they request?

**Objective:** To identify the most active travel agencies and analyse the types of travel services they enquire about, including group tours, hotel accommodation, flight arrangements and itinerary planning.

By examining sender information, agency domains, enquiry subjects and email content, we can determine how frequently individual agencies contact Turtle Down Under and categorise their service requirements.

**Business Value:** This analysis will help identify frequently engaged travel partners, understand their service preferences and recognise recurring patterns in travel requirements.

The findings may also support relationship management, targeted service offerings and operational resource planning based on agency demand.

## 5. Are travel agents primarily requesting Australia, New Zealand or combined travel packages?

**Objective:** To classify travel enquiries according to their destination requirements and analyse the frequency of repeated enquiries and follow-up communications from individual travel agencies.

We can identify whether agents are requesting Australian itineraries, New Zealand itineraries or combined Australia–New Zealand packages. We can also track how frequently the same agency follows up on an existing enquiry.

**Business Value:** This analysis will provide insights into destination preferences, recurring customer requirements and the frequency of communication associated with particular travel packages.

It will also help the company understand which destinations generate the highest enquiry activity and identify agencies that regularly request specific travel arrangements.

## 6. What passenger numbers and group sizes are requested by different travel agencies?

**Objective:** To extract and analyse passenger counts and group-size requirements mentioned in travel enquiries.

Using text extraction, we can identify group sizes from email subjects and message content, including references to adults, children, passenger numbers and group bookings.

**Business Value:** This analysis will enable the company to distinguish between agencies that primarily request smaller travel groups and those that frequently organise larger group movements.

The findings can support supplier coordination, accommodation planning, transport arrangements and the identification of potential high-volume travel opportunities.

## 7. Which enquiries involve the most email exchanges and longest discussions?

**Objective:** To identify enquiries with high communication volumes and extended discussion periods, and examine the factors contributing to their complexity.

This analysis will evaluate the number of messages, conversation duration, frequency of follow-ups and nature of the information requested throughout each enquiry.

We can investigate whether agents repeatedly request similar information, require multiple itinerary revisions, seek additional clarification or introduce new requirements during the discussion.

**Business Value:** Understanding these communication patterns will help identify potential operational bottlenecks, recurring information gaps and opportunities to improve quotation and enquiry-handling processes.

It will also provide insights into travel-agent communication behaviour and distinguish between genuinely complex bookings and enquiries experiencing avoidable delays.

## 8. How many emails are promotional, automated or potentially irrelevant to business enquiries?

**Objective:** To establish a business-specific email classification framework that separates genuine travel enquiries from promotional messages, automated notifications, delivery failures and potentially unwanted correspondence.

We can develop structured classification rules and prompt engineering techniques based on Turtle Down Under's operational requirements.

The classification framework will distinguish between:

- **Business Enquiries:** Genuine requests for quotations, bookings, itineraries and travel services.
- **Promotional Emails:** Marketing campaigns, newsletters and supplier advertisements.
- **Automated Emails:** Out-of-office responses, automatic acknowledgements and system-generated notifications.
- **Delivery Failures:** Undeliverable messages and email delivery error notifications.
- **Potential Junk:** Unsolicited, suspicious or irrelevant messages that do not contribute to business operations.

**Business Value:** This analysis will help improve email data quality, reduce unnecessary inbox clutter and ensure that operational reporting focuses on genuine business communications.

It will also enable the company to develop consistent criteria for identifying non-enquiry messages while preserving relevant supplier and system notifications.

## 9. Which enquiries involve quotations, booking confirmations or cancellations?

**Objective:** To identify and classify enquiries according to key booking-related activities, including quotation requests, quotation revisions, booking confirmations and cancellations.

By analysing email content and conversation history, we can identify travel agents who frequently request quotations, progress towards booking confirmations or communicate booking cancellations after extended discussions.

**Business Value:** This analysis will help the company understand the communication patterns associated with different stages of the enquiry and booking process.

It can also identify enquiries involving repeated quotation revisions, lengthy confirmation discussions and cancellation-related correspondence.

These findings may support improvements in quotation preparation, follow-up procedures and booking coordination. Where booking-system records are available, the analysis could be extended to examine actual enquiry-to-booking conversion rates.

---

## Overall Project Outcome

The proposed analysis aims to transform unstructured email correspondence into measurable business insights covering enquiry management, travel-agent engagement, operational responsiveness and travel service demand.

By combining Python-based data processing, natural language processing, structured prompt engineering and business intelligence visualisation, the project will support the identification of communication patterns, operational inefficiencies and opportunities for process improvement.

The results can be presented through an interactive dashboard, enabling Turtle Down Under to monitor enquiry volumes, agent activity, response times, destination preferences, group requirements and booking-related communications.

**Implementation Consideration:** Enquiry matching, status classification and booking-related outcomes will require validation against business rules and, where available, operational booking records to ensure the resulting metrics are accurate and reliable.

***Auther Qasim Nasir***
