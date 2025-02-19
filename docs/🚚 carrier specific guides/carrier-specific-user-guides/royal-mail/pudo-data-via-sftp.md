---
title: Set up PUDO data via SFTP
excerpt: >-
  The _Pick Up and Drop Off (PUDO)_ service facilitates customers to collect or
  drop off their shipments at designated locations instead of waiting for home
  delivery. These locations can include retail stores, parcel lockers, or
  shipping facilities, offering greater convenience and flexibility for
  customers. PUDO services are particularly beneficial for those who may not
  always be available for direct delivery, helping to reduce missed delivery
  attempts and enhance overall customer satisfaction.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The PUDO SFTP (Secure File Transfer Protocol) integration involves establishing a secure connection that enables data exchange between SAPIENT and Royal Mail PUDO service. This integration facilitates the exchange of crucial information, such as drop-off locations, opening and closing times, and shipment tracking details in a secure manner.

> 🚧 _Important_
> 
> _If you want to set up the PUDO integration, make sure to meet the following prerequisites:_ 
> 
> - _[Enable PUDO integration](https://docs.intersoftsapient.net/docs/integration-activation) via the Royal Mail **Integration Activation** screen._
> - _Create a location for us to connect, and then raise a request to our onboarding team for PUDO data via SFTP by providing your RSA Public Key. Based on the details provided, our team will respond back with your connection details._

The PUDO SFTP solution provides you with all locations in a single file that you can store as a library. The file is generated on a daily basis— the structure and its contents are explained in the following sections.

## File Naming

All tracking data files will use the following naming conventions.

The elements in the filename are defined as follows:

| Element | Details                     |
| :------ | :-------------------------- |
| RM      | Royal Mail                  |
| LC      | Local Collect               |
| YYY     | Year date of file creation  |
| MM      | Month date of file creation |
| DD      | Day date of file creation   |

> For example, a file generated on 09th September 2019 at 5.32pm would be "RMLC20190909.CSV".

***

## File Structure Overview

Each file consists of a full list of available locations each day. Everyday, these files replace the previous days files.

***

## File Format

The file is saved in the CSV format with comma delimiters.  
The following table describes the records and fields that are present in the data file for each PUDO location.

***

## Header Record

| \# | Name        | Type | Max Length | Comments                                                                 |
| :- | :---------- | :--- | :--------- | :----------------------------------------------------------------------- |
| 1  | Record Type | C    | 1          | This will always be H                                                    |
| 2  | Date        | D    | 8          | Represents the date when the file was created in the format**ddmmyyyy**. |
| 3  | PO Records  | D    | 6          | Represents the number of Post Office records contained in the file.      |
| 4  | CSP Records | D    | 6          | Represents the number of CSP Records contained in the file.              |

***

## Detailed Record

[block:parameters]
{
  "data": {
    "h-0": "\\#",
    "h-1": "Name",
    "h-2": "Type",
    "h-3": "Max Length",
    "h-4": "Comments",
    "0-0": "1",
    "0-1": "Record Type",
    "0-2": "C",
    "0-3": "1",
    "0-4": "This will always be D",
    "1-0": "2",
    "1-1": "Office Type",
    "1-2": "C",
    "1-3": "3",
    "1-4": "Represents the values of either CSP (for RM Customer Service Points) or POL(for Post Offices).",
    "2-0": "3",
    "2-1": "Office number/refence",
    "2-2": "D",
    "2-3": "7",
    "2-4": "Represents the unique identifier for the office.",
    "3-0": "4",
    "3-1": "Office Name",
    "3-2": "C",
    "3-3": "50",
    "3-4": "Represents the name of the office.",
    "4-0": "5",
    "4-1": "Address Line 1",
    "4-2": "C",
    "4-3": "50",
    "4-4": "Represents the first line of address.",
    "5-0": "6",
    "5-1": "Address Line 2 (if relevant)",
    "5-2": "C",
    "5-3": "50",
    "5-4": "Represents the second line of address, if applicable.",
    "6-0": "7",
    "6-1": "Address Line 3 (if relevant)",
    "6-2": "C",
    "6-3": "50",
    "6-4": "Represents the third line of address, if applicable.",
    "7-0": "8",
    "7-1": "Address Line 4 (if relevant)",
    "7-2": "C",
    "7-3": "50",
    "7-4": "Represents the fourth line of address, if applicable.",
    "8-0": "9",
    "8-1": "Address Line 5 (if relevant)",
    "8-2": "C",
    "8-3": "50",
    "8-4": "Represents the fifth line of address, if applicable.",
    "9-0": "10",
    "9-1": "Town",
    "9-2": "C",
    "9-3": "50",
    "9-4": "Represents the name of the town.",
    "10-0": "11",
    "10-1": "Postcode",
    "10-2": "C",
    "10-3": "10",
    "10-4": "Represents the postcode of the location.",
    "11-0": "12",
    "11-1": "Longitude (if available)",
    "11-2": "C",
    "11-3": "10",
    "11-4": "Represents the longitude value for the office location, if applicable.",
    "12-0": "13",
    "12-1": "Latitude (if available)",
    "12-2": "C",
    "12-3": "10",
    "12-4": "Represents the latitude value for the office location, if applicable.",
    "13-0": "14",
    "13-1": "Monday Open 1",
    "13-2": "D",
    "13-3": "5",
    "13-4": "Represents the first opening time on Monday in the hh:mm (24hr clock) format.",
    "14-0": "15",
    "14-1": "Monday Open 2",
    "14-2": "D",
    "14-3": "5",
    "14-4": "Represents the second opening time on Monday in the hh:mm (24hr clock) format.  \n  \n_Note: This record is left blank if the office has only one opening time._",
    "15-0": "16",
    "15-1": "Monday Open 3",
    "15-2": "D",
    "15-3": "5",
    "15-4": "Represents the third opening time on Monday in the hh:mm (24hr clock) format.  \n  \n_Note: This record is  left blank if the office only has one or two opening times._",
    "16-0": "17",
    "16-1": "Monday Close 1",
    "16-2": "D",
    "16-3": "5",
    "16-4": "Represents the first closing time on Monday in the hh:mm (24hr clock) format.",
    "17-0": "18",
    "17-1": "Monday Close 2",
    "17-2": "D",
    "17-3": "5",
    "17-4": "Represents the second closing time on Monday in the hh:mm (i24hr clock) format.  \n  \n_Note: This record is left blank if the office has only one closing time._",
    "18-0": "19",
    "18-1": "Monday Close 3",
    "18-2": "D",
    "18-3": "5",
    "18-4": "Represents the third closing time on Monday in the hh:mm (24hr clock) format.  \n  \n_Note: This record is left blank if the office has only one or two closing times._",
    "19-0": "20",
    "19-1": "Tuesday Open 1",
    "19-2": "D",
    "19-3": "5",
    "19-4": "First opening time on Tuesday in format hh:mm (in 24hr clock format)",
    "20-0": "21",
    "20-1": "Tuesday Open 2",
    "20-2": "D",
    "20-3": "5",
    "20-4": "Second opening time on Tuesday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)",
    "21-0": "22",
    "21-1": "Tuesday Open 3",
    "21-2": "D",
    "21-3": "5",
    "21-4": "Third opening time on Tuesday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)",
    "22-0": "23",
    "22-1": "Tuesday Close 1",
    "22-2": "D",
    "22-3": "5",
    "22-4": "First Closing time on Tuesday in format hh:mm (in 24hr clock format)",
    "23-0": "24",
    "23-1": "Tuesday Close 2",
    "23-2": "D",
    "23-3": "5",
    "23-4": "Second Closing time on Tuesday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)",
    "24-0": "25",
    "24-1": "Tuesday Close 3",
    "24-2": "D",
    "24-3": "5",
    "24-4": "Third Closing time on Tuesday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)",
    "25-0": "26",
    "25-1": "Wednesday Open 1",
    "25-2": "D",
    "25-3": "5",
    "25-4": "First opening time on Wednesday in format hh:mm (in 24hr clock format)",
    "26-0": "27",
    "26-1": "Wednesday Open 2",
    "26-2": "D",
    "26-3": "5",
    "26-4": "Second opening time on Wednesday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)",
    "27-0": "28",
    "27-1": "Wednesday Open 3",
    "27-2": "D",
    "27-3": "5",
    "27-4": "Third opening time on Wednesday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)",
    "28-0": "29",
    "28-1": "Wednesday Close 1",
    "28-2": "D",
    "28-3": "5",
    "28-4": "First Closing time on Wednesday in format hh:mm (in 24hr clock format)",
    "29-0": "30",
    "29-1": "Wednesday Close 2",
    "29-2": "D",
    "29-3": "5",
    "29-4": "Second Closing time on Wednesday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)",
    "30-0": "31",
    "30-1": "Wednesday Close 3",
    "30-2": "D",
    "30-3": "5",
    "30-4": "Third Closing time on Wednesday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)",
    "31-0": "32",
    "31-1": "Thursday Open 1",
    "31-2": "D",
    "31-3": "5",
    "31-4": "First opening time on Thursday in format hh:mm (in 24hr clock format)",
    "32-0": "33",
    "32-1": "Thursday Open 2",
    "32-2": "D",
    "32-3": "5",
    "32-4": "Second opening time on Thursday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)",
    "33-0": "34",
    "33-1": "Thursday Open 3",
    "33-2": "D",
    "33-3": "5",
    "33-4": "Third opening time on Thursday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)",
    "34-0": "35",
    "34-1": "Thursday Close 1",
    "34-2": "D",
    "34-3": "5",
    "34-4": "First Closing time on Thursday in format hh:mm (in 24hr clock format)",
    "35-0": "36",
    "35-1": "Thursday Close 2",
    "35-2": "D",
    "35-3": "5",
    "35-4": "Second Closing time on Thursday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)",
    "36-0": "37",
    "36-1": "Thursday Close 3",
    "36-2": "D",
    "36-3": "5",
    "36-4": "Third Closing time on Thursday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)",
    "37-0": "38",
    "37-1": "Friday Open 1",
    "37-2": "D",
    "37-3": "5",
    "37-4": "First opening time on Friday in format hh:mm (in 24hr clock format)",
    "38-0": "39",
    "38-1": "Friday Open 2",
    "38-2": "D",
    "38-3": "5",
    "38-4": "Second opening time on Friday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)",
    "39-0": "40",
    "39-1": "Friday Open 3",
    "39-2": "D",
    "39-3": "5",
    "39-4": "Third opening time on Friday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)",
    "40-0": "41",
    "40-1": "Friday Close 1",
    "40-2": "D",
    "40-3": "5",
    "40-4": "First Closing time on Friday in format hh:mm (in 24hr clock format)",
    "41-0": "42",
    "41-1": "Friday Close 2",
    "41-2": "D",
    "41-3": "5",
    "41-4": "Second Closing time on Friday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)",
    "42-0": "43",
    "42-1": "Friday Close 3",
    "42-2": "D",
    "42-3": "5",
    "42-4": "Third Closing time on Friday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)",
    "43-0": "44",
    "43-1": "Saturday Open 1",
    "43-2": "D",
    "43-3": "5",
    "43-4": "First opening time on Saturday in format hh:mm (in 24hr clock format)",
    "44-0": "45",
    "44-1": "Saturday Open 2",
    "44-2": "D",
    "44-3": "5",
    "44-4": "Second opening time on Saturday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)",
    "45-0": "46",
    "45-1": "Saturday Open 3",
    "45-2": "D",
    "45-3": "5",
    "45-4": "Third opening time on Saturday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)",
    "46-0": "47",
    "46-1": "Saturday Close 1",
    "46-2": "D",
    "46-3": "5",
    "46-4": "First Closing time on Saturday in format hh:mm (in 24hr clock format)",
    "47-0": "48",
    "47-1": "Saturday Close 2",
    "47-2": "D",
    "47-3": "5",
    "47-4": "Second Closing time on Saturday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)",
    "48-0": "49",
    "48-1": "Saturday Close 3",
    "48-2": "D",
    "48-3": "5",
    "48-4": "Third Closing time on Saturday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)",
    "49-0": "50",
    "49-1": "Sunday Open 1",
    "49-2": "D",
    "49-3": "5",
    "49-4": "First opening time on Sunday in format hh:mm (in 24hr clock format)",
    "50-0": "51",
    "50-1": "Sunday Open 2",
    "50-2": "D",
    "50-3": "5",
    "50-4": "Second opening time on Sunday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)",
    "51-0": "52",
    "51-1": "Sunday Open 3",
    "51-2": "D",
    "51-3": "5",
    "51-4": "Third opening time on Sunday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)",
    "52-0": "53",
    "52-1": "Sunday Close 1",
    "52-2": "D",
    "52-3": "5",
    "52-4": "First Closing time on Sunday in format hh:mm (in 24hr clock format)",
    "53-0": "54",
    "53-1": "Sunday Close 2",
    "53-2": "D",
    "53-3": "5",
    "53-4": "Second Closing time on Sunday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)",
    "54-0": "55",
    "54-1": "Sunday Close 3",
    "54-2": "D",
    "54-3": "5",
    "54-4": "Third Closing time on Sunday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)"
  },
  "cols": 5,
  "rows": 55,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


> 🚧 _Important_
> 
> _Each office can have up to a maximum of 3 opening windows in a day. Therefore, the open/close profiles for any day may vary as shown in the following tables._

| Name    | Opening/closing times |
| :------ | :-------------------- |
| Open 1  | 07:30                 |
| Open 2  | 13:00                 |
| Open 3  | 18:00                 |
| Close 1 | 12:00                 |
| Close 2 | 17:00                 |
| Close 3 | 20:00                 |

***

| Name    | Opening/closing times |
| :------ | :-------------------- |
| Open 1  | 07:30                 |
| Open 2  | 13:00                 |
| Open 3  |                       |
| Close 1 | 12:00                 |
| Close 2 | 17:00                 |
| Close 3 |                       |

***

| Name    | Opening/closing times |
| :------ | :-------------------- |
| Open 1  | 07:30                 |
| Open 2  |                       |
| Open 3  |                       |
| Close 1 | 18:00                 |
| Close 2 |                       |
| Close 3 |                       |

> 📘 _Note_
> 
> _For more information on how to use this API endpoint, refer to the [PUDO Locations](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode) API reference. However, based on your requirements, you can use the SFTP solution as well. _
> 
> > _For instance,  if you want to find the PUDO locations for one postcode at a time, for example to integrate with the checkout feature on their website, then the API would be the more suitable solution. On the contrary, if you want to download the PUDO data into your own system to check the PUDO locations that are close by to a given address by yourself, then the SFTP solution would be more suitable._