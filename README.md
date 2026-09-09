Process Automation Steps (BP Tool VMT automation) 
We receive a request for a specific region id – ex: N-Japan-H3573
STEP 1: Chek the attached attachments and the BPTool Data Matching or Not
Required documents – Vendor quote, SOW, Customer PO, NCRT(if balance is low we can ask for ncrt file)
1.1 Quotation ID matching or not
1.	Check what all the documents that they have uploaded
2.	The quotation id is supposed(we can see the quotation number in PORLIST table) to match with the copy of the document provided
1.2: PO start date and End date (PO Duration)
1.	The Date present in the attached document should match with the dates present in the BPTOOL List
Start Date,  End Date

1.3: PO Value
1.	The po value should match i.e in quotation and in the BPTool the PO values should match
PO_value_LC
How many resources involved total resource cost is matched or not while comparing to previous request

If a new resource then we need to drop an email and ask for justification 
1.4 Quote Validity
•	If the date is future date then there is no problem 
•	If the PO start Date is in past then it is ATF request we need write them the mail asking for the regional lead approval (why there is delay in raisinf the request as the PO start date is in past)
  
ATF Approval Request - Within Same Month
Japan & APeJ - Ishimoto-San
EMEA - Alessando Perot
AMS - Joseph Lyhn
 
ATF Request - Raised in Previous Month
"Mark Colaluca"
1.4: SOW Document
Check whether sow document is attached or not

Step 2:
2.1 Check the Category under which the request is raised
CL- OSC/T&M
If it is a OSC overall the will allocate the cost (not working based on FTE)
T&M model is like monthly salary fixed amount per resourse ( monthly cost for resourse)
NON CL:
No resourses involved here it is like service based 
Rental, OEM, Royalty, Resale, R&D

2.2 Check whether it is a renewal request or  not
If it is renewal request then they will provide the old po number/ BPTOOL ID
If it is a new resource then they wont provide any po number

If it is a Renewal Request then we need to compare the existing request with the current request 
If the request is raised under the same project ID then there is no issue	
Else we need to check the PO END Date i.e old PO END DATE is past date and the new PO Start Date is Future Date then it is fine 
If not we need to discuss it in daily calls then move forward


ResourceRequestList this sharepoint list contains the all the line items regarding the resources involved in the project
Resource Name, FTE, Cost Rate
STEP 3: Cost and Revenue Projection
If the ID is available in the ResourceRequestList that indicates that they have completed the step 3 
If they haven’t completed the step 3 then we have to drop them an email indicating that they haven’t completed the step 3 

Step 4: Validate whether the 3P cost is matched the Request or Not
For this we can refere the WWD list
The 3P cost must be inline with the planned 3P cost lc if it is not inline then we have to drop an email 
We can calculate the overall cost = total amount of all the request raised under same project id

If all things are ok then we go to the edit page and approve the request 

For Non cl request no need to validate the resource we can just validate the quote and if the quote is valid then we can proceed 
For cl requests we need to validate the  resource whether the resource is on hold or not and whether the resource can be allocated or not






Request Received
▼
Validate Documents
├─ Quotation ID Match
├─ PO Dates Match
├─ PO Value Match
├─ Quote Validity Check
└─ SOW Attached
▼
Validate Request Type
├─ CL (OSC/TNM)
└─ NON-CL
▼
Check Renewal Logic
├─ Same Project → Continue
├─ Valid Date Gap → Continue
└─ Else Daily Call Discussion
▼
Step 3 Completed?
(ResourceRequestList)
├─ No → Send Email
└─ Yes
▼
Validate 3P Cost (WWD List)
├─ Cost Mismatch → Send Email
└─ Cost Match
▼
CL Request?
│
├─ Yes → Validate Resource Availability
└─ No → Validate Quote Only
│
▼
Approve Request





the above is what i noted in the meeting and below is the documet that my manager sent
 PO Request Validation Points 

CL PO Requests: 

Attached Documents Validation (Vendor SOW, Quote, Customer PO) 

BPTool Request PO Start & End Date, Value, Currency should be matched with Quote/Vendor SOW. 

BPTool Customer PO Number should be matched with Attached Customer PO Copy. 

If it’s a Renewal PO request, they need to update Existing PO Number. 

If DWO Approved “Yes”, They supposed to add DWO Approved email. 

PO Start Date is in Past, they suppose to add comments under “ATF Justification” Why there is delay. 

Project Margin should not be negative. 

 

Non – CL PO Requests: (Resale/Rental/OEM/Royalty/R&D-License-OEM) 

Attached Documents Validation (Quote, Customer PO) 

Need to check the validity of the Quote. 

If it’s a Renewal PO request, they need to update Existing PO Number. 

If DWO Approved “Yes”, They supposed to add DWO Approved email. 

PO Start Date is in Past, they supposed to add comments under “ATF Justification” Why there is delay. 

For R&D PO Request, we suppose to add the Internal Project ID based on “PO For”. 

Project Definition 

Project Description 

C/294629 

ctg_PT_ENGG_NAVS 

C/294632 

ctg_PT_ENGG_Architecture Tool & Method 

C/294633 

ctg_PT_SUPPORT_BSS 

C/294637 

ctg_PT_SUPPORT_RI 

C/294634 

ctg_PT_SUPPORT_GMT 

C/294628 

ctg_PT_ENGG_BSS 

C/294630 

ctg_PT_ENGG_RI 

C/304402 

ctg_PT_ENGG_Continuous Impr & Compl 

C/294631 

ctg_PT_ENGG_SI 

C/294636 

ctg_PT_SUPPORT_NAVS 

Project Margin should not be negative. 

 

 

For OT – Over Time – Need to ask queries as below. 

*Please share the OT timesheet and hourly rate how the value is calculated. 
*What is the difference of base rate and Overtime effort rate. 
*Justification for Overtime. 

  




<img width="328" height="377" alt="{6399DA8E-F61C-4ADF-8869-B1FFE1F463A6}" src="https://github.com/user-attachments/assets/cd44328f-b614-49ab-9f15-a8e7c34a3433" />

<img width="326" height="396" alt="{8EF7041C-5A77-4F45-A74B-DA66A64E73A0}" src="https://github.com/user-attachments/assets/9d7ec9b3-715c-4e61-9014-a7ec630c215d" />


<img width="313" height="406" alt="{CADB4085-9FDF-4BB8-9F56-333E379EB06B}" src="https://github.com/user-attachments/assets/7e9258d5-7c5a-42a9-8af8-eada63f9321b" />



 


















