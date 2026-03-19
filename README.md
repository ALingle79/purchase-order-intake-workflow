# Automated Purchase Order Intake Workflow

## Overview

This project documents a process improvement initiative that replaced an unstructured email-based purchase order request process with a standardized intake form, automated routing workflow, and supporting dashboard.

The solution combines **Microsoft Forms**, **Power Automate**, **SharePoint**, and **Power BI** to improve the accuracy, consistency, and speed of purchase order intake and ERP entry.

## Problem

Purchase order requests were originally submitted through email. Important details and attachments were often spread across messages or located in separate systems, which made the process time-consuming and inconsistent.

To enter a request into the ERP system, financial analysts had to:

* gather information from multiple sources
* locate and verify attachments
* switch between several screens to piece together the required details
* manually organize the information before entry

This created unnecessary manual effort and increased the risk of delays or missed information.

## Solution

I redesigned the intake process by building a Microsoft Form and pairing it with a Power Automate flow.

The workflow:

* captures standardized request data from Microsoft Forms
* parses uploaded attachment metadata
* retrieves files from SharePoint
* compiles a structured email with the required details and attachments
* supports downstream ERP entry with cleaner, more complete information

I also built a Power BI dashboard that surfaces additional reference data required for ERP entry—information that is not available to the original requester at submission time. The dashboard brings together these supplemental details with the submitted request so financial analysts can complete ERP entry without switching between multiple systems.

## Tools Used

* Microsoft Forms
* Power Automate
* SharePoint Online
* Power BI
* Outlook

## Workflow Summary

1. User submits a purchase order request through Microsoft Forms.
2. Power Automate retrieves the response details.
3. The flow parses the JSON output for uploaded attachments.
4. The flow loops through each attachment and retrieves the file content from SharePoint.
5. The flow compiles the request information and attachments into a structured email.
6. Financial analysts use the email and dashboard to complete ERP entry more efficiently.

## Technical Highlights

* Parsed a JSON array returned by Microsoft Forms for uploaded files
* Used **Apply to each** to process attachments dynamically
* Built dynamic file retrieval logic for SharePoint-hosted form uploads
* Structured email attachments correctly for Outlook delivery
* Troubleshot attachment formatting issues to prevent corrupted PDF files
* Created a Power BI dashboard to centralize request details for downstream users

## Business Impact

* Replaced an unstructured email-based intake process with a standardized workflow
* Reduced manual effort required to gather request information
* Improved consistency of submitted data and attachments
* Made ERP entry faster and more straightforward for financial analysts
* Created a foundation for future reporting on request volume and turnaround time

## Screenshots

Suggested screenshots:

1. Microsoft Form overview
2. Power Automate flow overview
3. Attachment handling section of the flow
4. Power BI dashboard overview

## Future Enhancements

* Add error handling and notification for failed file retrievals
* Log request status for process monitoring
* Expand Power BI reporting to track turnaround time and bottlenecks
* Add request history and summary metrics

## Repository Structure

```text
purchase-order-intake-workflow/
├── README.md
├── images/
│   ├── form-overview.png
│   ├── flow-overview.png
│   ├── attachment-logic.png
│   └── dashboard-overview.png
└── notes/
    └── implementation-notes.md
```

## How to Use This Repository

This repository is intended as a portfolio project that demonstrates:

* process improvement
* workflow automation
* document handling
* dashboard design
* business-focused problem solving

## Project Summary

Designed and implemented an automated purchase order intake workflow using Microsoft Forms, Power Automate, SharePoint, and Power BI, replacing a manual email-based process with a standardized system that improved data consistency, reduced processing effort, and streamlined ERP entry.
