You are a documentation architect for GoHighLevel systems.  
Using the **Core & Spoke Naming Blueprint** and the **SOP structure from the PAV Module**, create a complete SOP for a new module.  

The SOP must include the following sections:  
1.0 Purpose and Scope — Why the module exists, what it covers (in-scope vs. out-of-scope), and the intended audience.  
2.0 Asset Inventory — Full list of assets organized by type (Funnels, Forms, Calendars, Workflows, Email Templates, SMS Snippets).  
   - All assets must be named with the module prefix `[ModulePrefix]` and placed in a folder `[Spoke] – [Module Name]`.  
   - Include page breakdown for Funnels.  
3.0 Custom Value Dictionary — List Core values (global brand assets) and Spoke values (module-specific content).  
   - Core values follow the format `Core_Descriptor`.  
   - Spoke values follow the format `Spoke_[ModulePrefix]_[Asset]_[Element]_[Attribute]`.  
4.0 Workflow Logic — Step-by-step automation flow (trigger, emails, SMS, waits, tags, etc.).  
5.0 Funnel Page Requirements — Page-by-page purpose, content, and use of custom values.  
6.0 Deployment Checklist — A step-by-step list of tasks to set up and test the module.  
7.0 Governance Notes — Immutable keys, promotion rules (Spoke → Core), and Airtable dictionary logging.  
Appendix: Quick reference list of Core and Spoke keys.  

**Module Information (replace placeholders):**  
- Module Name: [Module Name]  
- Module Prefix: [ModulePrefix]  
- Assets to include: [List the funnel pages, forms, calendars, workflows, emails, SMS snippets, etc.]  
- Required Core Values: [List global values like brand name, email sender, etc.]  
- Required Spoke Values: [List headlines, body text, video URLs, message subjects, etc.]  

Output the SOP as a structured document, with headings, checklists, and code-style formatting for all custom value keys. Follow the format of the `[PAV] Plan A Visit — Updated SOP`.  
