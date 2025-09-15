# Module Data Input Template (for SOP Prompt)

Use this template to collect the required data before running the SOP‑generation prompt. Fill in each section with details specific to your new module.

---

## 1. Module Identity

* **Module Name:** \[Reputation Management]
* **Module Prefix:** \[REP]

---

## 2. Asset Inventory

List all assets that will be created for this module.

### Funnels

* Funnel Name: \[Review Funnel] Update to match module name

  * Page 1: \[Review Page + Prompt for review submission but only pass to 3rd party site if 4-5 stars] Update to match module name + Purpose

### Survey

* \[REV Review Survey] — fields: 
  * `contact.rate_us` (1-5 stars) (update to match module name)
  * `contact.fullname`
  * `contact.email`
  * `contact.your_feedback` (update to match module name)

### Trigger Links
* \[Review Request Link] — purpose: Link to trigger review request workflow (update to match module name)
  * Link URL: \[`custom_value.review_request_link`] (update to match module name)

### Workflows

* \[1 - Past Customers - Ask For Review] — trigger: \[tag: Review Campaingn] Update to match module name + what starts it
* \[2 - Review Link Clicked] — trigger: \[link click: Review Request Link] Update to match module name + what starts it
* \[3 - Negative Feedback Recived] — trigger: \[contact submits REV Review Survey with 1-3 stars] Update to match module name + what starts it
* \[Ongoing Review Campaingn] - trigger: \ [tag: request review] Update to match module name + what starts it

### Email Templates

* \[Review Template 1] — purpose: \[Ask for review] Update to match module name + purpose (update to match module name)
* \[REP - Past Vistiors - Messsage 1] - purpose: \[Ask for review] Update to match module name + purpose (update to match module name)
* \[REP - Past Vistiors - Messsage 2] - purpose: \[Follow up reminder] Update to match module name + purpose (update to match module name)
* \[REP - Negative Feedback - Alert to Staff] - purpose: \[Internal alert for negative feedback] Update to match module name + purpose (update to match module name)
* \[REP - Negative Feedback - Response to Contact] - purpose: \[Response to negative feedback] Update to match module name + purpose (update to match module name)
* \[REP - Ongoing Review Campaign - Message 1] - purpose: \[Ask new visitors for a review request] Update to match module name + purpose (update to match module name)


### SMS Snippets

* \[REP - Past Vistiors - Text 1] — purpose: \[Ask for review] Update to match module name + purpose (update to match module name)
* \[REP - Past Vistiors - Text 2] — purpose: \[Follow up reminder] Update to match module name + purpose (update to match module name)
* \[REP - Ongoing Review Campaign - Text 1] — purpose: \[Ask new visitors for a review request] Update to match module name + purpose (update to match module name)
* \[REP - Ongoing Review Campaign - Text 2] — purpose: \[Follow up reminder] Update to match module name + purpose (update to match module name)


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


### 3.2 Spoke Values (Module-Specific)

Stored in folder: `[Spoke] – Connect Card`

| Key                                         | Description                                   |
| ------------------------------------------- | --------------------------------------------- |
| `Spoke_REP_Form_Survey_URL`               | URL of the Connect Card survey form           |
| `Spoke_REP_Email_Staff_Notification_Email` | Staff notification recipient email            |
| `Spoke_REP_Coordinator_First_Name`  | First name of the Connect Card coordinator          |
| `Spoke_REP_Coordinator_Last_Name`   | Last name of the Connect Card coordinator           |
| `Spoke_REP_Coordinator_Email` | Email of the Connect Card coordinator         |
| `Spoke_REP_Review_Google_URL`   | Public URL for Google review submission link     |
| `Spoke_REP_Trigger_Link`   | Public URL for the review request trigger link     |
| `Spoke_REP_Review_Request_Link`   | Public URL for the review request Funnel link     |



### 3.3 Spoke Contact Field (Module-Specific)
| Key                          | Description                                         |
| ---------------------------- | --------------------------------------------------- |
| `Spoke_REP_Rate_Us` | Star rating (1-5) submitted by contact in review survey |
| `Spoke_REP_Your_Feedback` | Text feedback submitted by contact in review survey |

---

## 4. Workflow Logic

* Workflow Name: \[1 - Past Customers - Ask For Review] Update to match module name
* **Trigger:** \[e.g., tag: Review Campaign]
* **Steps:**


* **Trigger:** \[e.g., Appointment confirmed]
* **Steps:**

  1. \[Action: SMS to visitor with review request link]
  2. \[Action: Email 1 to visitor with review request link\]
  3. \[Action: Wait 1 days\]
  4. \[Condition: if Review Link Clicked tag exists, go to step 7; else continue\]
  5. \[Action: SMS 2 to visitor with review request link\]
  6. \[Action: Email 2 to visitor with review request link\]
  7. \[Action: remove from current workflow\]
  8. \[end\]

* Workflow Name: \[2 - Review Link Clicked] Update to match module name
* **Trigger:** \[e.g., link click: Review Request Link]
* **Steps:**

  1. \[add tag: Review Link Clicked] (update to match module name)
  2. \[remove from workflow 1. Past Customers - Asked For Review\] (update tag to match module name)
  3. \[end]

* Workflow Name: \[3 - Negative Feedback Recived] Update to match module name
* **Trigger:** \[e.g., contact submits REV Review Survey with 1-3 stars\]
* **Steps:**
  
  1. \[Action: Remove from workflow 1. Past Customers - Asked For Review\] (update tag to match module name)
  2. \[Action: Send internal REP - Negative Feedback - Alert to Staff\]
  3. \[Action: Send REP - Negative Feedback - Response to Contact\]
  4. \[Action: remove from current workflow\]
  5. \[end\]

* Workflow Name: \[Ongoing Review Campaign] Update to match module name
* **Trigger:** \[e.g., tag: request review\]
* **Steps:** 

  1. \[Action: Wait 20 minutes\]
  2.  \[Action: SMS to visitor with review request link  (REP - Ongoing Review Campaign - Text 1)\]
  3. \[Action: Email 1 to visitor with review request link (REP - Ongoing Review Campaign - Message 1)\]
  4. \[Action: Wait 1 days\]
  5. \[Condition: if Review Link Clicked tag exists, go to step 8; else continue\]
  6. \[Action: SMS 2 to visitor with review request link (REP - Ongoing Review Campaign - Text 2)\]
  7. \[Action: Email 2 to visitor with review request link (REP - Ongoing Review Campaign - Message 2)\]
  8. \[Action: remove from current workflow\]
  9. \[end\]


---

## 5. Funnel Page Requirements

**Page 1: \[Review Page]** (update to match module name)

* Purpose: Capture review submission and redirect to 3rd party site if 4-5 stars
* Content:

  * Headline: How would you rate your experience at {{ Core_Church_Name }}?
  * Embed: `Spoke_CNC_Form_Survey_URL`
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
