# Module Data Input Template (for SOP Prompt)

Use this template to collect the required data before running the SOP‑generation prompt. Fill in each section with details specific to your new module.

---

## 1. Module Identity

* **Module Name:** \[Connect Card]
* **Module Prefix:** \ [CNC]

---

## 2. Asset Inventory

List all assets that will be created for this module.

### Funnels

* Funnel Name: \[Connect Card]

  * Step 1: \[CNC Start] used to connect CNC Survey
  * Step 2: \[CNC Thank you] used to display thank you and show a video


### Survey

* \[CNC Connect Card Survey] — fields: \[Last Name, First Name, Phone, Email, Address]

### Workflows
Workflow Folder Name: \[Connect Card]

* \[CC - 12 Week Follow Up - First Time Guests Workflow] — trigger: \[Survey Submitted, CNC Connect Card Info Survey]

### Email Templates

Current Folder Name: Connections System

* \[CNC - 01 Email Notification to Staff // Sends Immediately] 
   - purpose: Initial Email to staff to notify them someone has filled out a connect card and sends imidiatly after the survey is submitted. 
   - custom values:  \[contact.name, contact.phone, contact.email, Core_Church_Name, Core_Name_Sender_First, Core_Email_Sender, Connect Card Coordinator Name, Connect Card Staff Notification Email ]

* \[CNC - 02 Email Notification to Staff // Sends Monday AM // Selfie video] 
  - purpose: Email the staff first monday morning of the 12 week drip to remind them to send a personalized video to each new visitor that submited a connect card.  
  - custom values:  \[contact.name, contact.phone, contact.email, Core_Name_Sender_First, Core_Email_Sender, Connect Card Coordinator Name, Connect Card Staff Notification Email ]

* \[CC - 03 Email // Tuesday AM] 
  - purpose: The purpose of this email is to Reach out to the new visitor within the first week and see if there's anything that we can pray for them about and just a general follow-up or if they have any questions.  
  - custom values:  \[contact.name, Connect Card Coordinator Name , Core_Name_Sender_First, Core_Email_Sender` ]

* \[CC - 04 Email Notification to Staff // Wednesday AM // Written Note] 
  - purpose: The purpose of this email is to reach out to the staff Remind them to create a handwritten note to the recent new visitor and mail it to them or hand it to them in person next time they come to church.    
  - custom values:  \[contact.name, contact.email, contact.phone, contact.full_address, Core_Name_Sender_First, Core_Email_Sender, Connect Card Staff Notification Email]

* \[CNC - 05 Email // Week 2 - Monday 11am] 
  - purpose: To reach out to the contact of the new visitor on week 2 at the beginning of the week on Monday. See if they have any questions and let them know that you'd like to see them at the custom guest event. Fill it in with the variable.   
  - custom values:  \[contact.name, Connect Card Coordinator Name , Core_Name_Sender_First, Core_Email_Sender, Core_Church_Name ]

* \[CC - 06 Email Notification Week 2 to Staff // Sends Monday AM] 
  - purpose: To notify the pastor about the recent new visitor and have the pastor reach out with their new visitor's contact information.     
  - custom values:  \[contact.first_name, contact.name, contact.email, contact.phone, Core_Name_Sender_First, Core_Email_Sender, Core_Pastor_First_Name, Core_Pastor_Email, Connect Card Coordinator Name, Core_Church_Name]

* \[CC - 07 Email // Week 3 Thursday AM] 
  - purpose: To reach out to the visitor, let them know that they'd love to see them at the upcoming Sunday service and that there is an upcoming welcome party.      
  - custom values:  \[contact.first_name, Core_Name_Sender_First, Core_Email_Sender, Core_Email_Sender, Connect Card Coordinator Name, Core_Church_Name]

* \[CC - 08 Email // Week 11 Thursday AM] 
  - purpose: To reach out to the visitor see how things are going and if there is anything they can do for them or thier family.      
  - custom values:  \[contact.first_name, Core_Name_Sender_First, Core_Email_Sender, Core_Email_Sender, Connect Card Coordinator Name, Core_Church_Name]

* \[CC - 09 Email Notification to Staff // Week 13 Send 84 Days] 
  - purpose: To notify the staff that the new visitor has finished up their welcome 12-week drip campaign To log into the system and add them or remove them from any groups needed for continued communication.      
  - custom values:  \[contact.name, contact.email, contact.phone, Core_Name_Sender_First, Core_Email_Sender, Connect Card Coordinator Name]

### SMS Snippets

Current Folder Name: CNC Connect Card

* \[CNC - 01 text // Immediate // SMS Welcome] 
  - purpose: This text wishes them that they hope that they enjoy the rest of their visit, and then asks if they have stopped by the welcome center so that they can meet you and so that the visitor can pick up their free gift. 
  - custome Values: [contact.name, Core_Welcome_Center_Name]

* \[CNC - 02 Text // 4 days // Thursday AM] 
  - purpose: Reach out to the new visitor, seeing if there's anything they can pray for them for or if they need support on or if there are any questions they need to answer, and hoping that they see him this weekend at church. 
  - custome Values: [contact.name, Connect Card Coordinator Name, Core_Church_Name]

* \[CNC - 03 Text // Week 2 // Saturday PM] 
  - purpose: Reaching out to say they'd hope to see him at church tomorrow. 
  - custome Values: [contact.name, Connect Card Coordinator Name, Core_Church_Name]

* \[CNC - 04 Text // Week 3 // Saturday PM] 
  - purpose: Reaching out to say they'd hope to see him at church tomorrow. 
  - custome Values: [contact.name, Connect Card Coordinator Name, Core_Church_Name]

* \[CNC - 05 Text // Week 4 // Thursday AM Text] 
  - purpose: Just to check in to see how they're enjoying the church so far. 
  - custome Values: [contact.name, Connect Card Coordinator Name, Core_Church_Name]

* \[CNC - 06 Text // Week 5 // Tuesday PM Text] 
  - purpose: Check in to see how the church can pray for them this week. 
  - custome Values: [contact.name, Connect Card Coordinator Name]

* \[CNC - 07 Text // Week 6 // Saturday AM] 
  - purpose: Letting the visitor know that we've been preparing this week's message and are excited about it. We hope to see them at church and pose the question, "If they can make it?" 
  - custome Values: [contact.name, Core_Church_Name]

* \[CNC - 08 Text // Week 7 // Thursday AM] 
  - purpose: Just a general check-in to see if there's anything they can do for the visitor. 
  - custome Values: [contact.name, Connect Card Coordinator Name]

* \[CNC - 09 Text // Week 8 // Tuesday PM] 
  - purpose: Checking in with a visitor on behalf of the church, seeing how they can pray for them and their family this week. 
  - custome Values: [contact.name, Connect Card Coordinator Name, Core_Church_Name]

* \[CNC - 10 Text // Week 9 // Thursday PM] 
  - purpose: Letting the visitor know we have a great service planned at church, and we'd love to see them. Asking if they are able to make it. 
  - custome Values: [contact.name, Connect Card Coordinator Name, Core_Church_Name]

* \[CNC - 11 Text // Week 10 // Thursday PM] 
  - purpose: Reaching out to the visitor, letting them know they'd love to see him at the welcome party and asking if they can make it. 
  - custome Values: [contact.name, Connect Card Coordinator Name, Core_Church_Name]

* \[CNC - 12 Week 11 // Text Message // Thursday PM] 
  - purpose: Letting the visitor know we have a great service planned at church this weekend and asking if they'll be there. 
  - custome Values: [contact.name, Connect Card Coordinator Name]

* \[CNC - 13 Text Week 12 // Saturday PM] 
  - purpose: Reaching out to the visitor again, asking him to let him know that we'd love to see him there at church, and if they can make it. 
  - custome Values: [contact.name, Connect Card Coordinator Name, Core_Church_Name]

---

## 3. Custom Values

### Core Values (Global)

* `Core_Church_Name`
* `Core_Email_Sender`
* `Core_Name_Sender_First`
* `Core_Name_Sender_Last`
* (Optional) `Core_URL_Logo`, `Core_Address_Full`, `Core_Phone_Main`
* `Core_Pastor_Email`
* `Core_Pastor_First_Name`
* `Core_Welcome_Center_Name`

### Spoke Values (Module‑Specific)

* Connect Card Coordinator Name
* Unique URLs or media (e.g., confirmation video)
* Connect Card Staff Notification Email
* guest_event_name

---

## 4. Workflow Logic

* **Trigger:** \[CNC Connect Card Info Survey submitted]
* **Steps:**

  1. Set event start date to now
  2. Send Welcome Text to visitor after submittion [CNC - 01 text // Immediate // SMS Welcome]
  3. send notification email to staff [CNC - 01 Email Notification to Staff // Sends Immediately]
  4. Condtion if current day of the week is Monday and time is 10am then send go to next step if not loop back to top of condtion
  5. Set contact custom field cnc-week = to 1
  6. Send internal Email [CNC - 02 Email Notification to Staff // Sends Monday AM // Selfie video]
  7. wait 24 hours
  8. Send Visitor an email [CC - 03 Email // Tuesday AM] 
  9. Wait 24 hours
  10. Send Internal Email [CC - 04 Email Notification to Staff // Wednesday AM // Written Note]
  11. Wait 24 hours
  12. Send Vistior SMS [CNC - 02 Text // 4 days // Thursday AM] 
  13. Wait 4 Days
  14. Set contact custom field cnc-week = to 2
  15. Sent Visitor email [CNC - 05 Email // Week 2 - Monday 11am]
  16. Send Internal email [CC - 06 Email Notification Week 2 to Staff // Sends Monday AM]
  17. Wait 5 days and 5 hours
  18. Send SMS to visitor [CNC - 03 Text // Week 2 // Saturday PM]
  19. Wait 1 day and 19 hours
  20. Set contact custom field cnc-week = to 3
  21. wait 3 days
  22. Send visitor an email [CC - 07 Email // Week 3 Thursday AM]
  23. Wait 2 days and 5 hours
  24. Send visitor sms [CNC - 04 Text // Week 3 // Saturday PM]
  25. Wait 1 day and 19 hours
  26. Set contact custom field cnc-week = to 4
  27. wait 3 days
  28. Send visitor sms [CNC - 05 Text // Week 4 // Thursday AM Text]
  29. Wait 4 days
  30. Set contact custom field cnc-week = to 5
  31. wait 1 days and 5 hours
  32. Send visitor sms [CNC - 06 Text // Week 5 // Tuesday PM Text]
  33. Wait 5 days and 19 hours
  34. Set contact custom field cnc-week = to 6
  35. wait 5 days
  36. Send visitor sms [CNC - 07 Text // Week 6 // Saturday AM]
  37. Wait 2 days
  38. Set contact custom field cnc-week = to 7
  39. wait 3 days
  40. Send visitor sms [CNC - 08 Text // Week 7 // Thursday AM]
  41. Wait 4 days
  42. Set contact custom field cnc-week = to 8
  43. wait 1 days and 5 hours
  44. send visitor sms [CNC - 09 Text // Week 8 // Tuesday PM]
  45. Wait 5 days and 19 hours
  46. Set contact custom field cnc-week = to 9
  47. wait 3 days and 5 hours
  48. send visitor sms [CNC - 10 Text // Week 9 // Thursday PM]
  49. Wait 3 days and 19 hours
  50. Set contact custom field cnc-week = to 10
  51. wait 3 days and 5 hours
  52. send visitor sms [CNC - 11 Text // Week 10 // Thursday PM]
  53. Wait 3 days and 19 hours
  54. Set contact custom field cnc-week = to 11
  55. Wait 3 days
  56. send visitor email [CC - 08 Email // Week 11 Thursday AM]
  57. wait 5 hours
  58. send visitor sms [CNC - 12 Week 11 // Text Message // Thursday PM]
  59. Wait 3 days and 19 hours
  60. set contact custom field cnc-week = to 12
  61. wait 5 days and 5 hours
  62. send visitor sms [CNC - 13 Text Week 12 // Saturday PM]
  63. Wait 1 day and 19 hours
  64. set contact custom field cnc-week = to 13
  65. send internal email [CC - 09 Email Notification to Staff // Week 13 Send 84 Days] 


---

## 5. Funnel Page Requirements

* **Page 1:** 
  - Purpose: Landing page to link to CNC Connect Card Info Survey
  - content requirements: 
    * Headline: We are so glad you've joined us!
    * Subheadline: We'd love to connect with you! Take just a moment to give us your contact information so we can get to know you and let you know how we can best help you.
    * Logo: Core_URL_Logo
    * Embed: CNC Connect Card Info Survey
* **Page 2:** 
  - Purpose: Thank you page after survey submission
  - content requirements: 
    * Headline: Thank you for connecting with us!
    * Subheadline: We look forward to connecting with you! Someone from the church will be in touch soon.
    * Body text: In the meantime, check your email soon and reply back with any questions you have.
    * Logo: Core_URL_Logo
    * Video: Custom Connect Card video link to be provided by the church


---

## 6. Deployment Checklist

* [ ] Create folders under `[Spoke] – [Module Name]`
* [ ] Import funnel, forms, workflows, emails, SMS
* [ ] Configure Core values
* [ ] Configure Spoke values
* [ ] Test end‑to‑end flow
* [ ] Activate and hand off

---

## 7. Governance Notes

* Immutable Keys: never rename custom value Keys once created.
* Promotion Rule: promote Spoke → Core only if 2+ unrelated modules use it.
* Module/Value Database Governance: log all assets and values before creation.

---

**Tip:** Once this template is filled in, copy the data into the SOP Prompt Template to generate a complete Core & Spoke–aligned SOP for the module.
