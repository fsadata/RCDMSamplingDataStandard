#Raw Cows Drinking Milk Sampling Results Data Standard

### What Is This Document?

This document describes the data standard for submitting raw cows drinking milk (RCDM) sampling results data to the Food Standards Agency. It describes the fields, their data types and order and provides guidance on the acceptable range of values or controlled vocabularies which are required for individual fields.

This document does not describe the mechanism by which data can be submitted to the Food Standards Agency (the FSA).

### Who Is This Document For?

This document is written for Laboratory users who need to submit raw cows drinking milk sampling results data to the FSA.

### How This Document Is Structured

- [Sampling Results Standard Overview](#sampling-results-standard-overview) Contains a brief overview of all the fields in the standard.
- [Field Definitions](#field-definitions) Complete definitions for each field in the standard, includes constraints and specific data type formatting requirements.  
 1. [Sample ID](#1-sample-id)  
 2. [Producer ID](#2-producer-id) 
 3. [Lab](#3-lab)
 4. [Test Type](#4-test-type)
 5. [Test Result](#5-test-result)  
 6. [Sample Pass](#6-sample-pass)  
 7. [Sample Stage](#7-sample-stage)   
 8. [Sample From](#8-sample-from)  
 9. [CPH](#9-cph)  
 10. [Producer Name](#10-producer-name)  
 11. [Sample Date and Time](#11-sample-date-and-time) 
 12. [Sample Temperature at Collection](#12-sample-temperature-at-collection)
 13. [Receipt at Lab](#13-receipt-at-lab) 
 14. [Testing Date and Time](#14-testing-date-and-time)  
 15. [Sample Temperature at Testing](#15-sample-temperature-at-testing)
 16. [Report Date and Time](#16- report-date-and-time)  
- [Supported File Types](#supported-file-types)
- [Other Requirements](#other-requirements)
- [File Naming Conventions](#file-naming-conventions)

  
## Sampling Results Standard Overview

The following table lists the fields (name and description), their data types, whether they are optional, and whether they use a controlled vocabulary.

Index | Field Name | Description | Data Type | Optional | Controlled Vocabulary | Source
------|------------|-------------|-----------|----------|-----------------------|-------
1|sample_id|Sample unique identifier|Text|No|No|Lab
2|producer_id|producer unique identifier|Text|No|No|Lab
3|lab|The lab which undertook testing|Text|No|No|Lab
4|test_type|The type of test|Text|No|Yes|Lab
5|test_result|The result of the test|Text|No|No|Lab
6|sample_pass|Confirmation that sample passed or failed|Text|No|Yes|Lab
7|sample_stage|The stage in the sampling process|Text|No|Yes|Lab
8|sample_from|Where the sample was taken from|Text|No|Yes|Lab
9|cph|County parish holding number of producer|Text|No|No|Lab
10|producer_name|Name of producer|Text|No|No|Lab
11|sample_date_and_time|Date and time that the sample was taken|Datetime|No|No|Lab
12|sample_temperature_at_collection|Temperature of the sample when collected|Text|No|No|Lab
13|receipt_at_lab|Date and time sample received at lab|Datetime|No|No|Lab
14|testing_date_and_time|Date and time that the testing started|Datetime|No|No|Lab
15|sample_temperature_at_testing|Temperature of the sample when tested|Text|No|No|Lab
16|report_date_and_time|Date and time that the data is submitted to the FSA|Datetime|No|No|Lab

## Field Definitions

### 1. Sample ID
**Field Name:** `sample_id`  
**Data Type:** Text (32 character limit)  
**Optional:** No  
**Source:** Lab 
**Comments:** The sample number, as recorded by the laboratory carrying out the tests. This must be a unique value within the records of that lab. It can be any combination of numeric or alphanumeric characters but it must be unique within the laboratory system. 

 ### 2. Producer ID
**Field Name:** `producer_id`  
**Data Type:** Text (32 character limit)  
**Optional:** No  
**Source:** Lab 
**Comments:** The unique Producer reference number supplied to the laboratory by the FSA when a new producer is registered for the production of raw cows drinking milk. The reference will be quoted in the documentation accompanying the sample when the laboratory receives it.

### 3. Lab
**Field Name:** `lab`  
**Data Type:** Text (32 character limit)  
**Optional:** No  
**Source:** Lab 
**Comments:** The lab location which undertook the testing of the sample.

### 4. Test Type
**Field Name:** `test_type`  
**Data Type:** Text (controlled vocabulary)    
**Optional:** No  
**Source:** Lab 
**Comments:** The acceptable values for all tests will be provided by the FSA as a controlled vocabulary in a publicly available register. 

### 5. Test Result
**Field Name:** `test_result`  
**Data Type:** Text (controlled vocabulary)    
**Optional:** No  
**Source:** Lab 
**Comments:** The numeric figure giving the result of the test undertaken.

### 6. Sample Pass
**Field Name:** `sample_pass`  
**Data Type:** Text (controlled vocabulary)    
**Optional:** No  
**Source:** Lab 
**Comments:** `True` or `False`, determined by whether or not the sample passed the respective test.

### 7. Sample Stage
**Field Name:** `sample_stage`  
**Data Type:** Text (controlled vocabulary)    
**Optional:** No  
**Source:** Lab 
**Comments:** An indicator of the current stage in the sampling process. Acceptable values in this field are: 
For indicator testing only: 
- `Routine`
 - `Follow Up 1`
 - `Follow Up 2`
For full pathogen testing: 
- `Routine`
 - `Follow-up`
 - `Incident`

### 8. Sample From
**Field Name:** `sample_from`  
**Data Type:** Text (controlled vocabulary)    
**Optional:** No  
**Source:** Lab 
**Comments:** Describes the location from which the sample was taken. Acceptable values in this field are:
 - `FPCONT` or `Final Product Container`
 - `Bulk Tank`

### 9. CPH
**Field Name:** `cph`  
**Data Type:** Text (32 character limit)  
**Optional:** No  
**Source:** Lab 
**Comments:** The County Parish Holding number of the producer. This will be supplied to the laboratory by the FSA when a new producer is registered for  production of raw cows’ drinking milk. The CPH will be quoted in the documentation accompanying the sample when the laboratory receives it.

### 10. Producer Name
**Field Name:** `producer_name`  
**Data Type:** Text (50 character limit)  
**Optional:** No  
**Source:** Lab 
**Comments:** The name of the producer of the RCDM being sampled.

### 11. Sample Date and Time
**Field Name:** `sample_date_and_time`  
**Data Type:** Datetime
**Optional:** No  
**Source:** Lab 
**Comments:** The date and time at which the sample was taken.

### 12. Sample Temperature at Collection
**Field Name:** `sample_temperature_at_collection `  
**Data Type:** Text 
**Optional:** No  
**Source:** Lab 
**Comments:** The temperature of the sample at the time it was collected.

### 13. Receipt at Lab
**Field Name:** `receipt_at_lab`  
**Data Type:** Datetime  
**Optional:** No  
**Source:** Lab 
**Comments:** The date and time at which the sample was received by the lab.

### 14. Testing Date and Time
**Field Name:** `testing_date_and_time`  
**Data Type:** Datetime  
**Optional:** No  
**Source:** Lab 
**Comments:** The date and time at which the testing of the sample began.

### 15. Sample Temperature at Testing
**Field Name:** `sample_temperature_at_testing`  
**Data Type:** Text
**Optional:** No  
**Source:** Lab 
**Comments:** The temperature of the sample at the time it was tested.

### 16. Report Date and Time
**Field Name:** `report_date_and_time`  
**Data Type:** Datetime
**Optional:** No  
**Source:** Lab 
**Comments:** The date on which the results data was submitted to the FSA.

## Supported File Types

Currently we are supporting the standard for comma separated values (CSV) and JSON.

The [current standard for CSV](https://tools.ietf.org/html/rfc4180) gives a detailed explanation of the common format for CSV files. It's concise and clear and we recommend reading it.

## Other Requirements

### Text Fields

Most of the fields in the standard are text, which needs to be treated carefully when stored in a CSV file. All text fields must be enclosed within double quotes `"this is the text"`. You should try to avoid using double quotes within a text field as this can cause the field to be misread, but the RFC4180 standard allows it if handled appropriately.

>If double-quotes are used to enclose fields, then a double-quote appearing inside a field must be escaped by preceding it with another double quote. For example: `"aaa","b""bb","ccc"`

### Encoding

Where possible please use `UTF-8` encoding.

## File Naming Conventions

To make it easy for us to manage the files longer term, it will be important to name files so that we can tell the period that each file covers. The format will be the date and time of submission in `YYYYMMDD-HHMMSS` format.

For example, the file submitted the 31st of January 2017 15:20:33 would be named `20170131-152033.csv`.
