# Module Data Input Template (for SOP Prompt)

Use this template to collect the required data before running the SOP‑generation prompt. Fill in each section with details specific to your new module.

---

## 1. Module Identity

* **Module Name:** \[e.g., Next Steps]
* **Module Prefix:** \[e.g., NS]

---

## 2. Asset Inventory

List all assets that will be created for this module.

### Funnels

* Funnel Name: \[ ]

  * Page 1: \[Name + Purpose]
  * Page 2: \[Name + Purpose]
  * Page 3: \[Name + Purpose]

### Forms

* \[Form Name] — fields: \[list of fields]

### Calendars

* \[Calendar Name] — purpose: \[description]

### Workflows

* \[Workflow Name] — trigger: \[what starts it]

### Email Templates

* \[Template Name] — purpose: \[confirmation, reminder, follow‑up]

### SMS Snippets

* \[Snippet Name] — purpose: \[confirmation, reminder, etc.]

---

## 3. Custom Values

### Core Values (Global)

* `Core_Brand_Name`
* `Core_Email_Sender`
* `Core_Name_Sender_First`
* `Core_Name_Sender_Last`
* (Optional) `Core_URL_Logo`, `Core_Address_Full`, `Core_Phone_Main`

### Spoke Values (Module‑Specific)

* Funnel headlines, subheadlines, body text
* Workflow email subjects
* SMS body texts
* Unique URLs or media (e.g., confirmation video)

---

## 4. Workflow Logic

* **Trigger:** \[e.g., Appointment confirmed]
* **Steps:**

  1. \[Action: Email/SMS/Internal Alert]
  2. \[Action: Wait condition]
  3. \[Action: Tag or Branch]

---

## 5. Funnel Page Requirements

* **Page 1:** Purpose + content requirements
* **Page 2:** Purpose + content requirements
* **Page 3:** Purpose + content requirements

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
