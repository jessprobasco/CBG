# Module Data Input Template (for SOP Prompt)

Use this template to collect the required data before running the SOP‑generation prompt. Fill in each section with details specific to your new module.

---

## 1. Module Identity

* **Module Name:** \[Welcome Event]
* **Module Prefix:** \[WLE]

---

## 2. Asset Inventory

List all assets that will be created for this module.

### Funnels

* Funnel Name: \[WLE] - Welcome Event - Update to match module name

  * Page 1: \[Welcome Page + Prompt for new visitor information] Update to match module name + Purpose
  * Page 2: \[Welcome Event Thank You Page] Update to match module name + Purpose

### Form

* \[WLE Welcome Event Form] — fields: (update to match module name)
  * `contact.firstname`
  * `contact.lastname`
  * `contact.phone`
  * `contact.email`


### Workflows

* \[1 - New Visitors - Welcome Event] — trigger: \[form submission: WLE Welcome Event Form] Update to match module name + what starts it

### Email Templates

* \[WLE - Staff Notification - Message 1] — purpose: \[Notify staff of new visitor information] Update to match module name + purpose (update to match module name)
* \[WLE - New Visitors - Message 1] - purpose: \[Welcome new visitor and provide event details] Update to match module name + purpose (update to match module name)


### SMS Snippets

* \[WLE - New Visitors - Text 1] — purpose: \[Welcome new visitor and provide event details] Update to match module name + purpose (update to match module name)


---

## 3. Custom Values

### 3.1 Core Values (Global)

| CustomValueKey               | Description                             | Data Type |
| ---------------------------- | --------------------------------------- | --------- |
| `Core_Church_Name`           | Official church name                    | Text      |
| `Core_Email_Sender`          | Default sender email address            | Email     |
| `Core_Name_Sender_First`     | First name of default sender            | Text      |
| `Core_Name_Sender_Last`      | Last name of default sender             | Text      |
| `Core_Pastor_First_Name`     | Lead pastor’s first name                | Text      |
| `Core_Pastor_Last_Name`      | Lead pastor’s last name                 | Text      |
| `Core_Pastor_Email`          | Lead pastor’s email                     | Email     |
| `Core_URL_Logo`              | URL for primary church logo             | URL       |
| `Core_Welcome_Event_Name`   | Name of the main welcome event          | Text      |


### 3.2 Spoke Values (Module-Specific)

Stored in folder: `[Spoke] – Welcome Event`

| Key                                         | Description                                   |
| ------------------------------------------- | --------------------------------------------- |
| `Spoke_WLE_Location`               | Location of the welcome event           |
| `Spoke_WLE_Date`                   | Date of the welcome event         |
| `Spoke_WLE_Time`                   | Time of the welcome event         |
| `Spoke_WLE_Coordinator_First_Name`  | First name of the coordinator for the Welcome Event module          |
| `Spoke_WLE_Coordinator_Last_Name`   | Last name of the coordinator for the Welcome Event module           |
| `Spoke_WLE_Coordinator_Email` | Email of the coordinator for the Welcome Event module         |
| `Spoke_WLE_Event_Image_URL` | Public URL for an image of the event at the church         |


---

## 4. Workflow Logic

* Workflow Name: \[[WLE] - Welcome Event] Update to match module name
* **Trigger:** \[e.g., Form Submission: WLE Welcome Event Form]
* **Steps:**

  1. SMS → \[WLE - New Visitors - Text 1]
  2. Email → \[WLE - New Visitors - Message 1]
  3. Email → \[WLE - Staff Notification - Message 1]
  4. Tag Contact → \[e.g., Tag: Welcome Event Registered]
  5. Remove from Workflow → \[WLE - New Visitors - Welcome Event]
  6. End



---

## 5. Funnel Page Requirements

**Page 1: \[Welcome Event Landing Page]** (update to match module name)

* Purpose: Capture visitor information and provide event details
* Content:
  * Headline: Welcome to {{ Core_Church_Name }}! We're glad you're here.
  * Embed: `Spoken_WLE_Welcome_Event_Form`
  * Branding: `Core_URL_Logo`

**Page 2: \[Welcome Event Thank You Page]** (update to match module name)
* Purpose: Confirm submission and provide next steps
* Content:
  * Headline: Thank you for signing up!
  * Body: We look forward to seeing you at the {{ Spoke_WLE_Welcome_Event_Name }} on {{ Spoke_WLE_Date }} at {{ Spoke_WLE_Time }} located at {{ Spoke_WLE_Location }}.
  * Image of event at church: `Spoke_WLE_Event_Image_URL`
  * Branding: `Core_URL_Logo`
---

## 6. Deployment Checklist

* [ ] Create folders under `[Spoke] – [Module Name]`
* [ ] Import funnel, forms, workflows, emails, SMS
* [ ] Configure Core values
* [ ] Configure Spoke values
* [ ] Configure calendar availability
* [ ] Test end‑to‑end flow
* [ ] Activate and hand off

---

## 7. Governance Notes

* Immutable Keys: never rename custom value Keys once created.
* Promotion Rule: promote Spoke → Core only if 2+ unrelated modules use it.
* Airtable Governance: log all assets and values before creation.

---

**Tip:** Once this template is filled in, copy the data into the SOP Prompt Template to generate a complete Core & Spoke–aligned SOP for the module.
