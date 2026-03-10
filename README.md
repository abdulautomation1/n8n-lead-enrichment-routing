# Real-Time Lead Enrichment Engine

## Overview
In B2B sales, the first company to respond to a lead usually wins the deal. This n8n workflow eliminates manual research by instantly enriching new sign-ups with company data and prioritizing them for the sales team.

## Technical Workflow
- **Data Ingestion:** High-performance Webhook listener for real-time capture.
- **Third-Party Enrichment:** Apollo.io API integration to pull deep firmographic data (Employee count, Industry, LinkedIn URLs).
- **Data Consolidation:** Uses n8n **Merge nodes** to combine raw user input with enriched API metadata into a unified lead profile.
- **Conditional Routing:** Implements an automated scoring gate:
    - **High-Value (>50 employees):** Pushed to Slack for immediate engagement.
    - **General (≤50 employees):** Appended to Google Sheets for automated drip marketing.



## Impact
- **Response Time:** Reduced from several hours to <2 minutes for high-priority leads.
- **Data Quality:** 100% consistent data entry into the lead database via automated enrichment.
