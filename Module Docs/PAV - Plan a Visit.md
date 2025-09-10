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

* `Core_Church_Name`
* `Core_Email_Sender`
* `Core_Name_Sender_First`
* `Core_Name_Sender_Last`
* `Core_URL_Logo`
* `Core_Address_Full`
* `Core_Phone_Main`

### 3.2 Spoke Values (Module‑Specific)

* `Spoke_PAV_General_ConfirmationVideo_URL`
* `Spoke_PAV_Funnel_Start_Headline`
* `Spoke_PAV_Funnel_Start_Subheadline`
* `Spoke_PAV_Funnel_Calendar_Instructions`
* `Spoke_PAV_Funnel_Success_Headline`
* `Spoke_PAV_Funnel_Success_Body`
* `Spoke_PAV_Workflow_ConfirmationEmail_Subject`
* `Spoke_PAV_Workflow_24hEmail_Subject`
* `Spoke_PAV_Workflow_1hEmail_Subject`

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

*

---

## 7.0 Governance Notes

* **Immutable Keys:** Never rename custom value Keys after creation.
* **Promotion Rule:** Promote Spoke → Core only if ≥2 unrelated modules will use it.
* **Custom Value  Governance:** Log every asset and value in the custom value dictionary before creation.

---

### Appendix: Quick Reference Keys

**Core:** `Core_Brand_Name`, `Core_Email_Sender`, `Core_Name_Sender_First`, `Core_Name_Sender_Last`
**Spoke (PAV):** All funnel headlines, body text, workflow subjects, SMS texts, confirmation video URL
