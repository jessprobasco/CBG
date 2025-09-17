# \[Core] Values — SOP (Core & Spoke–Aligned)

**Module Name:** Core Values  
**Module Prefix:** Core  
**Version:** 1.1 (Updated)   
**Last Updated:** Sep 17, 2025  
**Owner:** Church Brand Guide Ops  

---

## 1.0 Purpose and Scope

**Purpose:**
Core Values are **global, brand-level custom values** that provide consistent identity, branding, and communication settings across all modules (Spoke systems). They act as the **immutable setup checklist** for every client account.

**Scope (In-Scope):**

* Fundamental church/brand identity fields
* Reusable values referenced by multiple modules (PAV, CNC, RepMan, etc.)
* Assets tied to branding, communication, and compliance

**Audience:**

* Agency implementers (snapshot setup)
* Church staff (brand/communications team)
* Developers automating workflows across modules

---

## 2.0 Folder Structure

All values must live in:
`[Core] – Brand Values`

No Core Values may exist outside this folder.

---

## 3.0 Custom Value Dictionary

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
| `Core_URL_Logo_Alt`          | URL for alternative church logo         | URL       |
| `Core_Phone_Main`            | Main public phone number                | Phone     |
| `Core_Address_Full`          | Full address (single line)              | Text      |
| `Core_Address_Full_Formatted` | Display-ready address (multi-line)      | Rich Text |
| `Core_Welcome_Center_Name`   | Name of Welcome Center / lobby location | Text      |
| `Core_Color_Primary_Hex`      | Primary brand color (hex code)          | Color Hex |
| `Core_Color_Secondary_Hex`    | Secondary brand color (hex code)        | Color Hex |
| `Core_Color_Tertiary_Hex`     | Tertiary brand color (hex code)         | Color Hex |
| `Core_Service_Times`         | Display text for service times          | Rich Text |
| `Core_Welcome_Event_Name`   | Name of the main welcome event          | Text      |

---

## 4.0 Usage

* **Funnels:** Logos, colors, service times, contact info
* **Workflows:** Global email sender name, pastor email, staff notifications
* **Emails/SMS:** Default sender identity, consistent signatures
* **Calendars:** Branding consistency for service/booking calendars

---

## 5.0 Governance Notes

* **Immutable Keys:** Never rename after creation.
* **Promotion Rule:** Only add new Core Values if used by 2+ unrelated modules.
* **Airtable Logging:** All Core Values must be logged in Airtable before deployment.
