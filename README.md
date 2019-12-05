### Introduction

- Standart of HCS Invoice;
- NOT FINALIED YET;
- Avoid putting to much data;
- Avoid data duplication;
- Data can be string type, which means text. Maximum 256 bytes for the one field of text. One symbol is 1 byte @https://en.wikipedia.org/wiki/ASCII;
- Data can be uint, which means digits. @https://en.wikipedia.org/wiki/Integer_(computer_science);
- Date is a uint too. @https://en.wikipedia.org/wiki/Unix_time;
- NO PRIVATE OR PERSONAL DATA!;

# Basic Invoice

![](https://media.licdn.com/dms/image/C4D0BAQFgcZL1_zQNnQ/company-logo_200_200/0?e=2159024400&v=beta&t=ZrXcAKVLTO6It7Oz3oPWoHMhmvnCbhItjWC8bdpS43E)

Templates:
https://drive.google.com/drive/folders/1orGvVcgdzbyK-zzQsKWswtLB8Y_eK7Lz

**Table of Contents**

[TOCM]

[TOC]

#Invoice Data
##Invoice Number
Number of the Invoice. What type it should be for the invoice to be easely adopt by final users?
Template for the number is needed.
First Header  | Second Header



| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceNumber`      | Seial Number of any Invoice.       | string or uint   | BCP120-4o2       |    

##Invoice Code

Spcial code that we found on templates. Maybe it an equivalent to Invoice Number?

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceCode`      | Seial Code of any Invoice.       | string or uint   | BCP120-4o2       |    
##Invoice Year

Defines year of Invoice creation.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceYearCreation`      | Year of Invoice creation.       |  uint8   | 2019       |    

##Invoice Date

Defines date of Invoice creation.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceDate`      | Year of Invoice creation.       | string or uint   | 2019.02.02       |    
##Bill To

Data Device Co. billing address.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceBillTo`      | Banking account.       | string or uint   | PJCB132IR142       |    

##Sold To

Data about Hospital's billing address.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceSoldTo`      | Banking account.       | string or uint   | PJCB132IR142       | 
##Purchase Order

**Was found in the templates. No idea about the meaning.**

##Credit Terms Code
Some specific info for the banking system.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceCreditTerms`      | Credit terms.       | string or uint   | 18       | 

##Due Date
When the devices should came to the buyer. **Invoice expires after that date?**

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceDueDate`      | Expiration Date.       | uint   | 2020.02.02       | 

#Seller
##Company
Information about Device Co.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceSellerCompay` | Full name with address?       | string   | Best Company LLC.       | 

##Cost Default Vendor
**Cost for the device**

##Request Location
Define final location of the device.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceRequestLocation` | Place where to ship the device.       | string   | The Best Place for Delievery st. 15      | 
##Requistation
**what data should be there**?
##Purchase From
**Who is the third party?**

#Buyer
##Cost Default Vendor
Default cost without comission, taxes, etc.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceCostDefault`      | Tax-free price.       | string or uint  | $1,111,111,111.12       | 
##Requisition Description
Some scpecial description for the Invoice.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceRequsutionDescr`      | Notes to the Invoice.       | string  | Bу carefull      | 
##Requester
Info about person or organization.
**Docter or Hopital?**
##Deliver To
The address where to deliever the device.
What difference between **Request Location**?

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceDelieverTo`      | Address.       | string  | Place for Devices       | 
#Invoice info Table:
##Item
###NAME
Name of a Device

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemDevice`      | Quck description.       | string  | Best Device       | 
###VENDOR
Seller name.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemVendor`      | Name of organization.       | string   | BestVendor LLC.       | 
###VENDOR ITEM
Special description for the Venor Co. Special code or something else.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemVendorItem`      | Code for Vendor.       | string or uint  | TX-15R2       | 
###GTIN
**???**
###Manufacurer Code
Special dexription for the Devce Co. Special code or something like that.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemManufCode`      | Code for Manufacturer.       | string or uint  | TX-15R2       | 
###PO Code
**???**
##Item Type
**???**
##UOM
**???**
##Unit Cost
Price for the one device.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceUnitCost`      | Unit tax-free price.       | string or uint  | $100       | 
##Extended Cost
Price with taxes, fees, etc.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemExtendedCost`      | Unit final price.       | string or uint  | $100       | 
##Distributions
**???**
##Activity / Account Category
**??**
##Distribution Allocation
**??**
##Requested Delievery Date
When is the time to deliever.
**what is the difference between Due Date**

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceRequestedDate`      | Final Date to deliever.       | string or uint  | 2020.02.02       | 
##Sourcing Event
**??**
##Quantity
**ATTENTION**
Should we use this field? Or we can create Invoice for any one device and unite them on the back-end?

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceQuantity`      | Amount of devices.       | uint8  | 155       | 
##Description
Brief description of the Invoice. Do we need

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceDescription`      | Note about the Invoice.       | string or uint  | Awesome Invoice       | 
