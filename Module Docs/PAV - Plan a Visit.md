# \[PAV] Plan A Visit — Updated SOP (Core & Spoke–Aligned)

**Module Name:** Plan A Visit
**Module Prefix:** PAV
**Version:** 1.1 (Updated)
**Last Updated:** Sep 4, 2025
**Owner:** Church Brand Guide Ops

---

## 1.0 Purpose and Scope

**Purpose:** 
Deliver a frictionless, automated system for prospective visitors to plan their first visit. Provides confirmation, reminders, and a success page to ensure visitors feel expected and valued.

**Scope (In-Scope):**
* Funnel with form capture, calendar scheduling, and success page
* Automated workflows for confirmation and reminders (email + SMS)
* Custom values for all visitor-facing text and media
* Calendar integration for service times
* Internal notifications to host team
* Post-visit follow-up handled by Next Steps module or Connect Card module

**Audience:**
* Implementers (agency staff building module)
* Church communications and guest services team
* Ministry leaders responsible for visitor experience

---

## 2.0 Asset Inventory

### 2.1 Folder Structure

All assets live in **\[Spoke] – Plan A Visit** unless noted otherwise.
Sub‑folders: Funnels, Forms, Workflows, Email Templates, SMS Snippets.

### 2.2 Assets

* **Funnels**

  * `[PAV] – Plan A Visit Funnel`

    * Page 1: `PAV Start`
    * Page 2: `Plan a Visit Calendar`
    * Page 3: `Plan a Visit Success Page`

* **Forms / Surveys**

  * `[PAV] – Plan A Visit Form`

* **Calendars**

  * `[PAV] – {{ Core_Church_Name }} Service Times`

* **Workflows**

  * `[PAV] – Plan A Visit (Confirmation & Reminders)`

* **Email Templates**

  * `[PAV] – Email: 01 - Confirmation`
  * `[PAV] – Email: 02 - 24‑Hour Reminder`
  * `[PAV] – Email: 03 - 1‑Hour Reminder`

* **SMS Snippets**

  * `[PAV] – SMS: 01 - Confirmation`
  * `[PAV] – SMS: 02 - 24‑Hour Reminder`
  * `[PAV] – SMS: 03 - 1‑Hour Reminder`

---

## 3.0 Custom Value Dictionary

### 3.1 Core Values (Global)

| Key | Description |
| --- | ----------- |
| `Core_Church_Name`          | Official church name            |
| `Core_Email_Sender`         | Default sender email address    |
| `Core_Name_Sender_First`   | First name of email sender      |
| `Core_Name_Sender_Last`    | Last name of email sender       |
| `Core_Pastor_First_Name`   | Lead pastor first name          |
| `Core_Pastor_Email`         | Lead pastor email address       |
| `Core_URL_Logo`             | URL for church logo             |
| `Core_Phone_Main`           | Main public phone number        |
| `Core_Address_Full`         | Full physical address           |

### 3.2 Spoke Values (Module‑Specific)

| Key | Description |
| --- | ----------- |
| `Spoke_PAV_General_ConfirmationVideo_URL` | Public URL for the confirmation video embedded on the success page or in emails |
| `Spoke_PAV_Funnel_Start_Headline` | Headline text shown on the PAV Start page |
| `Spoke_PAV_Funnel_Start_Subheadline` | Supporting subheadline text on the PAV Start page |
| `Spoke_PAV_Funnel_Calendar_Instructions` | Instructional copy shown on the calendar booking page |
| `Spoke_PAV_Funnel_Success_Headline` | Headline displayed on the success/thank-you page after booking |
| `Spoke_PAV_Funnel_Success_Body` | Body copy for the success/thank-you page (next steps, what to expect) |
| `Spoke_PAV_Coordinator_Name` | Name of the coordinator for the Plan A Visit module |
| `Spoke_PAV_Coordinator_Email` | Email of the coordinator for the Plan A Visit module |
| `Spoke_PAV_Workflow_24hEmail_Subject` | Subject line used for the 24-hour reminder email |
| `Spoke_PAV_Workflow_1hEmail_Subject` | Subject line used for the 1-hour reminder email |


---

## 4.0 Workflow Logic

**Workflow:** `[PAV] – Plan A Visit (Confirmation & Reminders)`

1. Trigger: Appointment confirmed in `[PAV] – Church Service Times`
2. Internal alert to host team
3. Send Email → `[PAV] – Email: Confirmation`
4. Send SMS → `[PAV] – SMS: Confirmation`
5. Wait until 24 hours before appointment
6. Send Email → `[PAV] – Email: 24‑Hour Reminder`
7. Send SMS → `[PAV] – SMS: 24‑Hour Reminder`
8. Wait until 1 hour before appointment
9. Send Email → `[PAV] – Email: 1‑Hour Reminder`
10. Send SMS → `[PAV] – SMS: 1‑Hour Reminder`
11. (Optional) Add tag `Visited – PAV` and branch to Next Steps module

---

## 5.0 Funnel Page Requirements

* **Page 1: PAV Start**
  Form embed `[PAV] – Plan A Visit Form`; headline/subheadline from Spoke values

* **Page 2: Calendar**
  Show slots from `[PAV] – Church Service Times`

* **Page 3: Success Page**
  Display success headline/body from Spoke values; embed `Spoke_PAV_General_ConfirmationVideo_URL` if provided

---

## 6.0 Deployment Checklist

* import module via GHL Snapshot funnel, form, workflow, emails, SMS
* Configure Core Values in `[Core] – Brand Values`
* Configure Spoke Values for Plan A Visit (form URL, video, coordinator email, etc.)
* Test submission flow: form → workflow → email/SMS → staff notifications
* Verify timing logic for 12-week drip
* QA across desktop and mobile
* Activate and document in Module Dictionary


---

## 7.0 Governance Notes

* **Immutable Keys:** Never rename custom value Keys after creation.
* **Promotion Rule:** Promote Spoke → Core only if ≥2 unrelated modules will use it.
* **Custom Value  Governance:** Log every asset and value in the custom value dictionary before creation.

---

### Appendix: Quick Reference Keys

**Core:** 
`Core_Church_Name`, `Core_Email_Sender`, `Core_Name_Sender_First`, `Core_Name_Sender_Last`, `Core_Pastor_First_Name`, `Core_Pastor_Email`, `Core_URL_Logo`, `Core_Phone_Main`, `Core_Address_Full`

**Spoke (PAV):**
`Spoke_PAV_General_ConfirmationVideo_URL`, `Spoke_PAV_Funnel_Start_Headline`, `Spoke_PAV_Funnel_Start_Subheadline`, `Spoke_PAV_Funnel_Calendar_Instructions`, `Spoke_PAV_Funnel_Success_Headline`, `Spoke_PAV_Funnel_Success_Body`, `Spoke_PAV_Coordinator_Name`, `Spoke_PAV_Coordinator_Email`, `Spoke_PAV_Workflow_24hEmail_Subject`, `Spoke_PAV_Workflow_1hEmail_Subject`
