# Staff Policy Acknowledgment System

**Digital compliance tracking for frontline employees — built with zero budget**

-----

## Project Overview

Frontline casino employees don’t have company email addresses or Microsoft 365 accounts, making digital acknowledgment of policy and operational updates nearly impossible through standard enterprise tools. This project documents the research, decision-making, and implementation of a free, audit-ready acknowledgment tracking system built entirely with existing tools.

-----

## Problem Statement

**The challenge:** How do you digitally track whether frontline employees have read and acknowledged operational updates — without email, without enterprise software access, and without any budget?

**Constraints identified:**

- Frontline staff have no company email accounts
- Frontline staff have no Microsoft 365 licenses
- HotSchedules (scheduling platform) did not include acknowledgment tracking in the property’s subscription tier
- UKG (workforce management) broadcast/acknowledgment module was not activated in the property’s contract
- Oracle HCM Communicate requires a separate paid subscription not available to the property
- No budget approved for new tools or software

-----

## Research & Platform Evaluation

Before building, I evaluated every platform already in use at the property:

|Platform     |Feature Available        |Limitation                                                   |
|-------------|-------------------------|-------------------------------------------------------------|
|HotSchedules |Message Board (broadcast)|No acknowledgment/read receipt in current tier               |
|UKG Pro      |Communication Broadcast  |Module not activated; requires admin/IT enablement           |
|Oracle HCM   |HCM Communicate          |Requires separate paid subscription                          |
|Microsoft 365|Forms with acknowledgment|Frontline staff lack M365 accounts — login wall blocks access|

**Conclusion:** No existing enterprise platform could deliver the required functionality within the property’s current contracts and licenses.

-----

## Solution

**Tool:** Microsoft Forms (free, available via existing management M365 account)  
**Access method:** QR code posted at time clock — no app download, no login required  
**Cost:** $0

### How It Works

1. Manager creates a new Microsoft Form for each update
1. Update content is posted within the QR code at the time clock
1. Employee scans QR code with personal phone camera
1. Employee enters full name and employee ID number
1. Employee selects “I acknowledge” confirming they have read and understood the update
1. Employee submits — response is captured instantly with timestamp
1. Manager exports responses to Excel to identify who has and has not responded

### Form Structure

|Field                                                     |Type                           |Required    |
|----------------------------------------------------------|-------------------------------|------------|
|Update content                                            |Text/Section                   |Display only|
|Full name and employee ID                                 |Text input                     |Yes         |
|I have read and understand this update and agree to comply|Single choice — “I acknowledge”|Yes         |

-----

## Key Design Decisions

**Why “Anyone can respond” instead of Caesars login required?**  
Switching to open access removes the Microsoft login wall that would block frontline staff without M365 accounts. The tradeoff is that the Name column in responses shows “anonymous” — however, the employee’s typed name and ID in the response field serves as the accountable record.

**Why QR code instead of a link?**  
Frontline employees don’t receive internal communications via email or chat. A printed QR code at the time clock meets employees where they already are — no distribution problem, no reliance on them checking any platform.

**Why a new form per update?**  
Keeping each update as its own form maintains clean, searchable records organized by topic and date. Responses don’t mix between updates, making audit exports straightforward.

**Why not Excel on a shared drive?**  
A shared kiosk or network drive approach requires physical device access and introduces risk of employees marking off coworkers. The QR/Forms approach works on personal devices with individual submissions and timestamps.

-----

## Outcome

- Zero-cost digital acknowledgment system operational same day
- Audit-ready Excel export with name, employee ID, timestamp, and acknowledgment response
- No IT involvement required
- No new software or licenses required
- Works on any smartphone with a camera — no app download needed
- Scalable: duplicate the form for each new update in under 5 minutes

-----

## Skills Demonstrated

- **Business process analysis** — identified workflow gap, defined requirements, evaluated solutions against real constraints
- **Platform research** — evaluated HotSchedules, UKG, Oracle HCM, and Microsoft Forms against feature availability and licensing reality
- **Constraint-based problem solving** — delivered a functional solution within a zero-budget, no-IT environment
- **Compliance thinking** — built with audit trail, documentation, and accountability tracking as core requirements
- **Process documentation** — end-to-end workflow designed for repeatability by any manager on the team

-----

## Replication Guide

To replicate this system at any property or organization:

1. Navigate to **forms.microsoft.com** and sign in with a management M365 account
1. Click **New Form** and title it with the update topic and date
1. Add a **Text** question: *“Enter your full name and employee ID”* — mark Required
1. Add a **Choice** question: *“I have read and understand this update and agree to comply”* with one option: *“I acknowledge”* — mark Required
1. Go to **Settings** → select **“Anyone can respond”**
1. Go to **Collect responses** → click the **QR code icon** → Download
1. Print the QR code and post at time clock alongside a printed copy of the update
1. Monitor responses via **View responses** → export to Excel for accountability tracking

-----

## Author

**Evin Thuman**  
Operations Supervisor | Caesars Entertainment  
29 years regulated gaming industry experience  
ISC2 Certified in Cybersecurity (CC)  
BS Business Management — University of Phoenix, Summa Cum Laude (GPA 3.97)
[LinkedIn] (https??www.linkedin.com/in/evin-thuman-5a3409a1 

