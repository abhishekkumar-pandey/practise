# steps that i came up with after the meeting
Process Automation Steps (BP Tool VMT automation) 
We receive a request for a specific region id – ex: N-Japan-H3573
STEP 1: Chek the attached attachments and the BPTool Data Matching or Not
1.1 Quotation ID matching or not
1.	Check what all the documents that they have uploaded
2.	The quotation id is supposed(we can see the quotation number in PORLIST table) to match with the copy of the document provided

1.2: PO start date and End date (PO Duration)
1.	The Date present in the attached document should match with the dates present in the BPTOOL List
Start Date,  End Date

1.3: PO Value
1.	The po value should match i.e in quotation and in the BPTool the PO values should match
PO_value_LC

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
CL- OSC/TNM
If it is a OSC then there must be a per material cost
TNM model is like monthly salary fixed amount per resourse ( monthly cost for resourse)
NON CL:
No resourses involved here it is service based 
Rental, OEM

2.2 Check whether it is a renewal request or  not
If it is renewal request then they will provide the old po number
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
The 3P cost must be non negative



## steps provided by manager 
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

  
