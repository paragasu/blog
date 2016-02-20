---
layout: post
title: MSSQL paging with CTE
date: 2013-02-17 02:50:14.000000000 +08:00
type: post
published: true
status: publish
categories:
- database
tags: []
meta:
  _edit_last: '5225680'
  _publicize_pending: '1'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
No LIMIT OFFSET as in PostgreSQL or MySQL.

    WITH cte AS
    (
      SELECT ROW_NUMBER() OVER(ORDER BY country ASC) AS RowNumber
      FROM company WHERE country='Malaysia'
    )
    SELECT * FROM cte
    WHERE RowNumber > 0 AND RowNumber < 100



