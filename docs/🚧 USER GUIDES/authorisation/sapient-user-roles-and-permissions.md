---
title: Recommended role-based access to SAPIENT actions
deprecated: false
hidden: false
metadata:
  robots: index
---
\<!DOCTYPE html>

\<html lang="en">
\<head>
&#x20;   \<meta charset="UTF-8">
&#x20;   \<meta name="viewport" content="width=device-width, initial-scale=1.0">
&#x20;   \<title>Merge Table Rows\</title>
&#x20;   \<style>
&#x20;       table \{
&#x20;           width: 50%;
&#x20;           border-collapse: collapse;
&#x20;       }
&#x20;       th, td \{
&#x20;           border: 1px solid black;
&#x20;           padding: 8px;
&#x20;           text-align: center;
&#x20;       }
&#x20;   \</style>
\</head>
\<body>
&#x20;   \<table>
&#x20;       \<tr>
&#x20;           \<th>Header 1\</th>
&#x20;           \<th>Header 2\</th>
&#x20;       \</tr>
&#x20;       \<tr>
&#x20;           \<td rowspan="2">Merged Row\</td>
&#x20;           \<td>Row 1, Column 2\</td>
&#x20;       \</tr>
&#x20;       \<tr>
&#x20;           \<td>Row 2, Column 2\</td>
&#x20;       \</tr>
&#x20;   \</table>
\</body>
\</html>