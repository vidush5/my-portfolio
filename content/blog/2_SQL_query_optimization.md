---
title: "SQL Query Optimization"
description: "Optimization Techniques"
dateString: Feb 2024
draft: false
weight: 106
---
### Use Indexes
Efficiently designed and consistently managed indexes can notably enhance query performance, enabling the database to swiftly locate and fetch data.

### Use Limit to retrieve data
Opt for selecting only essential columns with 'SELECT' rather than 'SELECT *' to minimize unnecessary data transfer and processing overhead.

### Avoid Sub Queries in WHERE clause
Subqueries, especially when returning a substantial number of rows, can be resource-intensive and complex to execute. Consider utilizing join operations or crafting a correlated subquery to achieve equivalent results, thereby optimizing performance.

### Steer clear of combining DISTINCT and GROUP BY in queries.
Using GROUP BY inherently ensures row distinctness, rendering the use of DISTINCT alongside GROUP BY redundant.

### Replace UNION with UNION ALL
For improved UNION operations, consider utilizing UNION ALL over UNION when duplicate elimination is unnecessary or can be managed post-operation. Reserve the use of DISTINCT for essential cases, as it entails additional sorting and row comparison processes.

### Avoid using UNION and DISTINCT at the same time
UNION inherently ensures distinct records, obviating the need for using DISTINCT alongside UNION.

### Avoid multiple Joins

### Use UNION ALL Instead of OR, this way INDEX will be used





