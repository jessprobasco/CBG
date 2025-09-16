The Agency Architect’s Blueprint: A Definitive Guide to the Core & Spoke Naming Convention for GoHighLevel

Introduction: From Ad-Hoc to Architecture

Your agency has made a pivotal strategic decision: to adopt the Hybrid Core & Spoke Naming Convention. This choice signals a move away from reactive, ad-hoc building and toward a future of proactive, scalable architecture. It is the foundational step in transforming your collection of funnels, workflows, and templates into a cohesive, manageable, and productized system.

This document is your official blueprint. It codifies the rules not only for custom values but for the entire GoHighLevel asset ecosystem—including funnels, forms, workflows, calendars, and the folders that house them. By implementing this unified architecture, you will create a system that is self-documenting, radically simplifies team collaboration, minimizes errors, and unlocks powerful automation.

⸻

Part I: The Unchanging Principles of System Design

The Core & Spoke model is built upon four foundational principles of the GoHighLevel platform:
	1.	The Immutable Key: When a custom value is created, GoHighLevel generates a permanent, machine-readable Key from its Name. This Key can never be changed, making initial naming a permanent architectural commitment.
	2.	Human vs. Machine: Names must be both human-readable and automation-friendly. Use underscores (_), avoid spaces, and ensure clarity.
	3.	The Folder-First Approach: Folder structure is not an afterthought; it is designed in tandem with naming to enforce organization.
	4.	The Snapshot Lifecycle: Core values serve as the client-specific setup checklist, while Spoke values contain the pre-built system logic.

⸻

Part II: The Core & Spoke Architecture for Custom Values

Core Values (Global Brand Assets)
	•	Structure: Core_Type_Descriptor
	•	Folder: All Core values must reside in Core Brand Values.
	•	Examples:
	•	Core_Brand_Name
	•	Core_Brand_Tagline
	•	Core_Phone_Main
	•	Core_Email_Support
	•	Core_URL_Logo
	•	Core_Link_BookingCalendar
	•	Core_Color_PrimaryHex
	•	Core_ID_FacebookPixel
	•	Core_Snippet_EmailFooter

Spoke Values (Module-Specific Components)
	•	Structure: Spoke_Module_Asset_Element_Attribute
	•	Folder: Each module has its own custom value folder named Spoke - [Module].
	•	Component Definitions:
	•	Module: Short prefix (e.g., RepMan, Onboarding)
	•	Asset: GHL asset type (e.g., Funnel, Workflow, Form)
	•	Element: Specific page, step, or component
	•	Attribute: Data piece (e.g., Headline, Link)
	•	Examples:
	•	Spoke_RepMan_Funnel_ReviewPage_Headline
	•	Spoke_RepMan_Workflow_Request_InitialSMSText
	•	Spoke_Onboarding_Form_Intake_HeaderTitle
	•	Spoke_Onboarding_Workflow_Welcome_EmailSubject

Decision Framework
	1.	Is it a fundamental brand asset? → Core
	2.	Will it be referenced by multiple unrelated modules? → Core
	3.	Is it tied to one module’s logic? → Spoke
	4.	Default to Spoke when in doubt.

⸻

Part III: The Core & Spoke Architecture for Assets & Folders

Folder Naming Convention
	•	Structure: [Category] - Descriptive Name
	•	Examples:
	•	Spoke - Reputation Management
	•	Spoke - New Client Onboarding
	•	[Core] - General Assets
	•	[Core] - Calendars

Asset Naming Convention
	•	Structure: [Module Prefix] - Descriptive Name
	•	Examples:
	•	Workflows: RepMan - Review Request Sequence
	•	Funnels: Onboarding - Intake Funnel
	•	Forms: Onboarding - Client Intake Form
	•	Email Templates: RepMan - Positive Review Request
	•	Calendars: [Core] - 30-Min Discovery Call

⸻

Part IV: The Implementation Playbook: Your Airtable Dictionary

Airtable Base Structure

Your Airtable base is the single source of truth. It must include:
	1.	Modules Table
	•	Module Name (e.g., Reputation Management)
	•	Module Prefix (e.g., RepMan)
	•	Description
	2.	Custom Values Table
	•	CustomValueKey (e.g., Spoke_RepMan_Funnel_Headline)
	•	Category (Core or Spoke)
	•	Module (linked if Spoke)
	•	Purpose/Description
	•	Data Type (Text, URL, Phone, etc.)
	•	Status (Active, Deprecated)
	3.	Assets Table
	•	Asset Name (e.g., RepMan - Review Request Funnel)
	•	Asset Type (Workflow, Funnel, Form, etc.)
	•	Module
	•	Folder Name (auto-generated)
	•	Purpose/Description

⸻

Conclusion: Building for the Future

By adopting and enforcing this Core & Spoke architecture, your agency is:
	•	Reducing onboarding time
	•	Simplifying collaboration
	•	Minimizing costly errors
	•	Building structural integrity for automation

This is not optional—it is the standard by which all future work will be measured.