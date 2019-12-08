### Introduction

- Standart of HCS Invoice;
- NOT FINALIZED YET;
- Avoid putting to much data;
- Avoid data duplication;
- Data can be string type, which means text. Maximum 256 bytes for the one field of text. One symbol is 1 byte @https://en.wikipedia.org/wiki/ASCII;
- Data can be uint, which means Unsigned INTeger. @https://en.wikipedia.org/wiki/Integer_(computer_science);
- Date is a uint too. @https://en.wikipedia.org/wiki/Unix_time;
- NO PRIVATE OR PERSONAL DATA!;

# Basic Invoice

![](https://media.licdn.com/dms/image/C4D0BAQFgcZL1_zQNnQ/company-logo_200_200/0?e=2159024400&v=beta&t=ZrXcAKVLTO6It7Oz3oPWoHMhmvnCbhItjWC8bdpS43E)

Templates:
https://drive.google.com/drive/folders/1orGvVcgdzbyK-zzQsKWswtLB8Y_eK7Lz

**Table of Contents**

# Invoice Data
## Invoice Number
The number of the Invoice. What's the format of the Invoice Number (which type of characters will be used)?
Template for the Invoice number is needed.


| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceNumber`      | Serial Number of any Invoice       | string or uint   | BCP120-4o2       |    

## Invoice Code

Invoice Code is a special code that we found on templates. Maybe Invoice Code is the same as the Invoice Number.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceCode`      | Serial Code of any Invoice       | string or uint   | BCP120-4o2       |    

## Invoice Year

Invoice Year is the year when the Invoice was originated.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceYearCreation`      | Year of Invoice generation       |  uint8   | 2019       |    

## Invoice Date

Invoice Date is the date when Invoice was generated.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceDate`      | Date of Invoice generation       | string or uint   | 10/7/2019       |    

## Bill To

Bill To is a special code. Example: "Bill To" code presented by Endologix is 30180 (top right corner).

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceBillTo`      | Special Code      | string or uint   | 30180       |    

## Sold To

Bill To is a special code. Example: "Sold To" code presented by Endologix is 30180 (top right corner).

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceSoldTo`      | Special Code       | string or uint   | 30180       | 

## Purchase Order

Purchase Order is a special code. Example: "Purchase Order" code presented by Endologix is blank (top right corner).

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoicePurchaseOrder`      | Special Code       | string or uint   | N/A      | 

## Credit Terms Code

Credit Terms Code is a special code. Example: "Credit Terms Code" presented by Endologix is N30 (top right corner).

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceCreditTerms`      | Special Code       | string or uint   | N30       | 

## Due Date

Due Date indicates the date on which an invoice is due.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceDueDate`      | Invoice Due Date     | uint   | 11/6/2019       | 

## Company

Company indicates Company Name and its special code.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceSellerCompany` | Company Name & Special Code      | string   | 0100 - Baystate Medical Center     | 

## Cost Default Vendor

Company Default Vendor might indicate a specific subsidiary.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceSellerCompany` | Company Default Vendor     | string   | B0256 - EDWARDS LIFESCIENCES LLC   | 

## Request Location

Request Location might indicate the internal code of a location.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceRequestLocation` | Request Location & Special Code      | string   | 400 - H&V OR DAVIS WING     | 

## Requisition

Requisition might indicate the internal code for an invoice.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceRequisition` | Internal code for an invoice    | string   | 2880705 - Unreleased   | 

## Purchase From

Purchase From - we don't know what that could mean.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoicePurchaseFrom` | ?  | string   | N/A   | 

## Buyer

Buyer might indicate an allocated individual within the Hospital.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoicePurchaseFrom` | Allocated purchaser within the Hospital  | string   | GAC - GARY CORDERO   | 


## Requisition Description

Requisition Description might indicate  a memo for the Invoice.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceRequsitionDescr`      | Invoice Memo       | string  | N/A      | 

## Requester

Requester - we don't know what that could mean.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceRequester`      | ?     | string  | EN17053 - James DiPinto    | 

## Deliver To

Deliver To might indicate the location to which devices should be delivered.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `invoiceDeliverTo`      | Delivery Address      | string  | N/A      | 

# Invoice Item Data:

## Item Code

Item Code is a special code for the device.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemDeviceCode`      | Item Code     | string  | D081041      | 

## Item Name

Item Name is the name of a device.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemDeviceName`      | Device Name      | string  | VALVE AORTIC PERIMOUNT SZ 25 / EACH       | 

## Vendor

Vendor is a Vendor organization.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemVendor`      | Vendor Organization       | string   | EDWARDS LIFESCIENCES LLC     | 

## Vendor Item

Vendor Item is a special code for a Vendor or a device. 

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemVendorItem`      | Special code      | string or uint  | 3300TFX25MM     | 

### GTIN

The Global Trade Item Number (GTIN) is an identified for trade items.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemGTIN`      | GTIN      | string or uint  | 00690103176155     | 

### Manufacturer Code

Manufacturer Code is a special code of a manufactturing organization.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemManufCode`      | Manufacturer Special Code       | string or uint  | 3300TFX25MM     | 

### PO Code

PO (Purchase Order) Code is a special code identifying a device.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemPOCode`      | PO Code      | string or uint  | GEN     | 

## Item Type

Item Type describes the type of an item.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemManufCode`      | Item Type     | string or uint  | Nonstock     | 

## UOM

UOM (Unit of Measurement) is a measurement code for Invoices.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemUOMCode`      | Unit of Measurement    | string or uint  | EA    | 

## Unit Cost

Unit Cost represents the price of a device.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `ItemUnitCost`      | Unit price       | string or uint  | $100.00       | 

## Extended Cost

Extended Cost is a price with taxes, fees, etc.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemExtendedCost`      | Unit final price      | string or uint  | $105.36     | 

## Distributions

Distributions - we don't know what that could mean.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemDistributions`      | ?    | string or uint  | 400-185533-0100    | 

## Activity / Account Category

Activity / Account Category - we don't know what that could mean.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemActivity`      | ?    | string or uint  | N/A   | 

## Distribution Allocation

Distribution Allocation - we don't know what that could mean.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemDistributionAlloc`      | ?    | string or uint  | 100.0%   | 

## Requested Delivery Date

Requested Delivery Date is a delivery date for the device.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemDeliveryDate`      | Final Delivery Date of the Device      | string or uint  | 10/18/2019      | 

## Sourcing Event

Sourcing Event - we don't know what that could mean.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemSourcingEvent`      | ?     | string or uint  | No     | 

## Quantity Ordered

Quantity Ordered is an ordered device quantity.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemQuantity`      | Quantity Ordered      | uint8  | 1       | 

## Description
Description is a brief description of the Item Ordered.

| Field name | Description                     | Blockchain Type   | Example           |
| ------------- | ------------------------------ |---------------------|------------------|          
| `itemDescription`      | Item Description     | string or uint  | Venapax XL Vessel Harvesting System       | 
