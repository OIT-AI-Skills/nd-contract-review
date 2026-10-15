# BuyND+ Contract Request Fields

The questions on the BuyND+ contract request form. Use the exact field labels in the report so the requester can match them to the form.

**Source** hints where the answer usually comes from:
- **Doc**: normally found in the contract documents. Fill it, cite the clause, and confirm.
- **Ask**: only the requester knows. Ask it.
- **Either**: try the documents first, then ask.

## Always-visible questions

| ID | Field | Type | Required | Source |
|---|---|---|---|---|
| Q1 | Originating Department | Dropdown (see Departments) | Yes | Ask |
| Q3 | Will a buyND requisition be created to pay for this contract? | Radio | Yes | Ask |
| Q5 | Is this contract a result of a Procurement-led sourcing event such as an RFP or an RFQ? | Radio | Yes | Ask |
| Q7 | Contract Summary (Please describe the contract's purpose.) | Text | Yes | Doc: a 2–3 sentence purpose statement, not the full analysis summary |
| Q8 | If any other buyND users from your department should be included as a stakeholder, please add their first and last name. | Text | No | Ask |
| Q10 | Start Date | Date | Yes | Either |
| Q11 | Update Start Date Upon Execution | Checkbox | No | Either: check when the contract starts on signature |
| Q12 | End Date | Radio: Expires On / Term / other | No | Doc |
| Q16 | What is the target date by which you wish to have this contract signed and in place? | Date | Yes | Ask |
| Q18 | If funding is necessary, what is the funding source? | Text | No | Ask |
| Q19 | Will federal and/or grant funding be used for any portion of this contract? | Radio | Yes | Ask |
| Q20 | Please add the first and last name of your authorized Notre Dame signer below. | Text | Yes | Ask |
| Q21 | If the contract requires a Second Party signature, please provide the signer's first and last name and email below. | Text | Yes | Either: check the signature block |
| Q22 | Second Party | Search (supplier lookup) | No | Doc: the vendor's legal name |
| Q23 | Additional Second Parties | Search | No | Doc |
| Q27 | Second Party Contact Name. This should be an individual from the Second Party who is the primary point of contact, but is not necessarily the signatory listed above. | Text | Yes | Either |
| Q28 | Second Party Contact Email | Text | Yes | Either |
| Q29 | Second Party Phone Number | Text | No | Either |
| Q30 | Were you able to find your Second Party in the field above? (If no, please click the Supplier Add Request link below) | Radio | Yes | Ask: they find out when searching BuyND+ |

## Conditional questions

Ask a conditional question only when its trigger holds.

| ID | Field | Type | Required | Shown when | Source |
|---|---|---|---|---|---|
| Q2 | This contract request relates to: | Radio | Yes | Q1 is any department except Athletics | Doc: use the contract type |
| Q4 | Requisition # | Text | Yes | Q3 = Yes; requisition has been submitted | Ask |
| Q6 | RFP # | Text | No | Q5 = Yes | Ask |
| Q9 | Who authorized departmental resource for this contract? | Dropdown | No | Q1 is Applied and Computational Mathematics and Statistics, Biological Sciences, Chemistry and Biochemistry, College of Science-Dean's Office, Mathematics, or Physics | Ask |
| Q13 | Auto-Renew | Radio | No | Q12 = Expires On or Term | Doc |
| Q14 | Renewal Term | Text and Dropdown | No | Q12 = Expires On or Term | Doc |
| Q15 | Renewals Remaining | Text | No | Q12 = Expires On or Term | Doc |
| Q17 | What is the anticipated total dollar value of the contract? | Text | Yes | Q1 is any department except Athletics | Doc: total across the full term, including renewals the requester expects to use |
| Q24 | Contract Purpose | Dropdown | Yes | Q1 = Mendoza College of Business | Ask |
| Q25 | Who is the contract for? | Radio | Yes | Q1 = Mendoza College of Business | Ask |
| Q26 | List of Directors that approved this contract | Text | Yes | Q1 = Mendoza College of Business | Ask |
| Q31 | Please enter the legal name of the supplier / 2nd party. (This contract request can not be processed until the supplier add has been submitted and processed.) | Text | Yes | Q30 = No | Doc. Tell the requester to submit a Supplier Add Request first |
| Q32 | Does this software have an Artificial Intelligence (AI) component, or is it Cloud Based or SaaS/IaaS? | Radio | Yes | Q2 = Software | Either |
| Q33 | Has this request been submitted to OIT for cloud security assessment? | Radio | Yes | Q32 = Yes | Ask |
| Q38 | Date submitted for OIT Review | Date | Yes | Q33 = Yes | Ask |
| Q39 | ServiceNow Request # | Text | Yes | Q33 = Yes | Ask |
| Q40 | This contract request cannot be reviewed until a cloud security assessment has been completed. You can request this assessment in ServiceNow. Click the help icon "?" for additional details | Checkbox (acknowledge) | Yes | Q33 = No | Ask. Tell the requester to request the OIT assessment in ServiceNow before submitting |
| Q34 | What type of data will be stored using this product? | Checkbox | No | Q32 = Yes | Either |
| Q35 | Will the vendor have access to the ND Data? If yes, please specify what they will have access to. If not, please enter "No". | Text | No | Q32 = Yes | Either |
| Q36 | Will the ND data reside on the supplier's servers? | Radio | No | Q32 = Yes | Either |
| Q37 | Service Category | Dropdown (see Service categories) | Yes | Q2 = Software | Either |
| Q41 | Does this contract relate to OIT technology or an OIT project? | Radio | Yes | Q2 = Software | Ask |
| Q42 | Will this software include integrations with major ND systems (e.g. Banner)? | Radio | Yes | Q2 = Software | Ask |
| Q43 | Is this standard edition software or enterprise edition software? | Radio | Yes | Q2 = Software | Either |
| Q44 | How many Licenses are being purchased for this request? | Text | No | Q43 answered | Doc |
| Q45 | Are there initial fees to be paid up front that will not be paid in future years? | Radio | Yes | Q43 answered | Doc |
| Q52 | How much? | Text | Yes | Q45 = Yes | Doc |
| Q46 | What will this contract cost each time it renews? | Text | Yes | Q43 answered | Doc |
| Q47 | Is this contract used to perform a Pilot or Product Evaluation? | Radio | No | Q43 answered | Either |
| Q48 | Is there a Current Agreement between the Supplier and Notre Dame? | Radio | Yes | Q43 answered | Ask |
| Q53 | Please attach the current Agreement here. | Upload | No | Q48 = Yes | Ask |
| Q49 | Who is the University Point of Contact? | Text | No | Q43 answered | Ask |
| Q50 | Who is your Contract Representative? | Dropdown | No | Q43 answered | Ask |
| Q51 | Does this contract also include services? | Radio | No | Q43 answered | Doc |

## Contract types

Software, Purchase of Services, Purchase of Goods, Non-disclosure, Travel and Events, Leases, Payments to University, Other.

## Service categories (Q37)

Administrative and Business; Communication and Collaboration; Desktop & Mobile Computing; Infrastructure; IT Professional Services; Security; Research; Teaching and Learning.

## Departments (Q1)

Alumni Association; Applied and Computational Mathematics and Statistics; Architecture; Arts and Letters; Athletics; Audit and Advisory Services; Biological Sciences; Campus Dining; Campus Ministry; Campus Safety and University Operations; Center for Social Concerns; Chemistry and Biochemistry; College of Science-Dean's Office; Controller's Group; DeBartolo Performing Arts Center; Development; Engineering; Executive Vice President; Facilities Design and Operations; Finance Division; Financial Aid; First Year of Studies; Freimann Life Science Center; General Counsel; Graduate School; Hesburgh Library; Human Resources; iNDustry Labs; Innovation Park; Institute for Educational Initiatives; Investment Office; Kaneb Center for Teaching and Learning; Keck Center for Transgene Research; Kellogg Institute for International Studies; Keough School of Global Affairs; Kroc Institute for International Peace Studies; Law Library; Law School; LEO; Licensing; Maintenance; Mathematics; McGrath Institute for Church Life; Mendoza College of Business; Morris Inn; Nanovic Institute for European Studies; Notre Dame Band; Notre Dame Global; Office of Information Technology; Office of Mission Engagement; Office of Pre-College Programs; Office of Public Affairs & Communications; Office of Research; Office of Strategic Planning and Inst Research; Office of Sustainability; Other; Physics; President's Office; Procurement Services; Provost; Psychology; Registrar; Risk Management and Safety; Security and Police; Shakespeare; Snite Museum of Art; St. Michael's Laundry; Student Accounts; Student Activities-Department/Office; Student Activities-Student Club; Student Affairs; TRiO; Undergraduate Admissions; Undergraduate Enrollment; University Catering; University Enterprise & Events; University Relations; Utilities; VenueND; Warehouse and Delivery Services.

When the requester names a department loosely ("Mendoza", "OIT"), map it to the closest entry and confirm.
