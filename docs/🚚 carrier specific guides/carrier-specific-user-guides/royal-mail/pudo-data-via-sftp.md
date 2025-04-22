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

> 🚧 *Important*
>
> *If you want to set up the PUDO integration, make sure to meet the following prerequisites:*
>
> * *[Enable PUDO integration](https://docs.intersoftsapient.net/docs/integration-activation) via the Royal Mail **Integration Activation** screen.*
> * *Create a location for us to connect, and then raise a request to our onboarding team for PUDO data via SFTP by providing your RSA Public Key. Based on the details provided, our team will respond back with your connection details.*

The PUDO SFTP solution provides you with all locations in a single file that you can store as a library. The file is generated on a daily basis— the structure and its contents are explained in the following sections.

> 💡 *Tip*
>
> *To learn more about the file structure and its data, refer to the following example file:*
>
> <HTMLBlock>{`
> <a href="https://docs.google.com/spreadsheets/d/1wiz8kcQlMscAj81c-OFOPh_3gkfOheLadDkt5GYyAKo/edit?usp=sharing" download="https://docs.google.com/spreadsheets/d/1wiz8kcQlMscAj81c-OFOPh_3gkfOheLadDkt5GYyAKo/edit?usp=sharing">• RMLC20241209</a>
> `}</HTMLBlock>

<br />

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

The file is saved in the CSV format with comma delimiters.\
The following table describes the records and fields that are present in the data file for each PUDO location.

***

## Header Record

<Table align={["left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        #
      </th>

      <th>
        Name
      </th>

      <th>
        Type
      </th>

      <th>
        Max Length
      </th>

      <th>
        Comments
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        1
      </td>

      <td>
        Record Type
      </td>

      <td>
        C
      </td>

      <td>
        1
      </td>

      <td>
        This will always be H
      </td>
    </tr>

    <tr>
      <td>
        2
      </td>

      <td>
        Date
      </td>

      <td>
        D
      </td>

      <td>
        8
      </td>

      <td>
        Represents the date when the file was created in the format**ddmmyyyy**.
      </td>
    </tr>

    <tr>
      <td>
        3
      </td>

      <td>
        PO Records
      </td>

      <td>
        D
      </td>

      <td>
        6
      </td>

      <td>
        Represents the number of Post Office records contained in the file.
      </td>
    </tr>

    <tr>
      <td>
        4
      </td>

      <td>
        CSP Records
      </td>

      <td>
        D
      </td>

      <td>
        6
      </td>

      <td>
        Represents the number of CSP Records contained in the file.
      </td>
    </tr>
  </tbody>
</Table>

***

## Detailed Record

<HTMLBlock>{`
<table style="width: 100%; border-collapse: collapse;">
<thead>
<tr>
  <th style="border: 1px solid #ddd; padding: 8px;">#</th>
  <th style="border: 1px solid #ddd; padding: 8px;">Name</th>
  <th style="border: 1px solid #ddd; padding: 8px;">Type</th>
  <th style="border: 1px solid #ddd; padding: 8px;">Max Length</th>
  <th style="border: 1px solid #ddd; padding: 8px;">Comments</th>
</tr>
</thead>
<tbody>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Record Type</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>This will always be D</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Office Type</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the values of either CSP (for RM Customer Service Points) or POL(for Post Offices).</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Office number/refence</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>7</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the unique identifier for the office.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>4</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Office Name</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>50</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the name of the office.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Address Line 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>50</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the first line of address.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>6</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Address Line 2 (if relevant)</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>50</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the second line of address, if applicable.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>7</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Address Line 3 (if relevant)</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>50</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the third line of address, if applicable.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>8</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Address Line 4 (if relevant)</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>50</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the fourth line of address, if applicable.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>9</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Address Line 5 (if relevant)</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>50</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the fifth line of address, if applicable.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>10</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Town</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>50</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the name of the town.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>11</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Postcode</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>10</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the postcode of the location.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>12</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Longitude (if available)</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>10</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the longitude value for the office location, if applicable.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>13</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Latitude (if available)</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>C</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>10</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the latitude value for the office location, if applicable.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>14</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Monday Open 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the first opening time on Monday in the hh:mm (24hr clock) format.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>15</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Monday Open 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the second opening time on Monday in the hh:mm (24hr clock) format.  </p>
<p><em>Note: This record is left blank if the office has only one opening time.</em></p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>16</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Monday Open 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the third opening time on Monday in the hh:mm (24hr clock) format.  </p>
<p><em>Note: This record is  left blank if the office only has one or two opening times.</em></p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>17</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Monday Close 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the first closing time on Monday in the hh:mm (24hr clock) format.</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>18</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Monday Close 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the second closing time on Monday in the hh:mm (i24hr clock) format.  </p>
<p><em>Note: This record is left blank if the office has only one closing time.</em></p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>19</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Monday Close 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Represents the third closing time on Monday in the hh:mm (24hr clock) format.  </p>
<p><em>Note: This record is left blank if the office has only one or two closing times.</em></p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>20</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Tuesday Open 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First opening time on Tuesday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>21</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Tuesday Open 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second opening time on Tuesday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>22</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Tuesday Open 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third opening time on Tuesday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>23</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Tuesday Close 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First Closing time on Tuesday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>24</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Tuesday Close 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second Closing time on Tuesday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>25</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Tuesday Close 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third Closing time on Tuesday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>26</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Wednesday Open 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First opening time on Wednesday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>27</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Wednesday Open 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second opening time on Wednesday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>28</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Wednesday Open 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third opening time on Wednesday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>29</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Wednesday Close 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First Closing time on Wednesday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>30</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Wednesday Close 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second Closing time on Wednesday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>31</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Wednesday Close 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third Closing time on Wednesday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>32</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Thursday Open 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First opening time on Thursday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>33</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Thursday Open 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second opening time on Thursday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>34</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Thursday Open 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third opening time on Thursday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>35</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Thursday Close 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First Closing time on Thursday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>36</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Thursday Close 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second Closing time on Thursday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>37</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Thursday Close 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third Closing time on Thursday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>38</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Friday Open 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First opening time on Friday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>39</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Friday Open 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second opening time on Friday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>40</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Friday Open 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third opening time on Friday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>41</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Friday Close 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First Closing time on Friday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>42</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Friday Close 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second Closing time on Friday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>43</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Friday Close 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third Closing time on Friday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>44</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Saturday Open 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First opening time on Saturday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>45</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Saturday Open 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second opening time on Saturday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>46</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Saturday Open 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third opening time on Saturday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>47</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Saturday Close 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First Closing time on Saturday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>48</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Saturday Close 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second Closing time on Saturday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>49</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Saturday Close 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third Closing time on Saturday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>50</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Sunday Open 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First opening time on Sunday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>51</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Sunday Open 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second opening time on Sunday in format hh:mm (in 24hr clock format) (will be blank if office only has one opening time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>52</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Sunday Open 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third opening time on Sunday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two opening times)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>53</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Sunday Close 1</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>First Closing time on Sunday in format hh:mm (in 24hr clock format)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>54</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Sunday Close 2</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Second Closing time on Sunday in format hh:mm (in 24hr clock format) (will be blank if office only has one Closing time)</p>
</td>
</tr>
<tr>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>55</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Sunday Close 3</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>D</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>5</p>
</td>
  <td style="border: 1px solid #ddd; padding: 8px;"><p>Third Closing time on Sunday in format hh:mm (in 24hr clock format) (will be blank if office only has one or two Closing times)</p>
</td>
</tr>
</tbody>
</table>
`}</HTMLBlock>

> 🚧 *Important*
>
> *Each office can have up to a maximum of 3 opening windows in a day. Therefore, the open/close profiles for any day may vary as shown in the following tables.*

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

> 📘 *Note*
>
> \_*For more information on how to use this API endpoint, refer to the [PUDO Locations](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode) API reference. However, based on your requirements, you can use the SFTP solution as well.*
>
> > *For instance,  if you want to find the PUDO locations for one postcode at a time, for example to integrate with the checkout feature on their website, then the API would be the more suitable solution. On the contrary, if you want to download the PUDO data into your own system to check the PUDO locations that are close by to a given address by yourself, then the SFTP solution would be more suitable.*