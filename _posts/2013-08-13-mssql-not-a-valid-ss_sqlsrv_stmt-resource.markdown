---
layout: post
title: "mssql not a valid ss_sqlsrv_stmt resource"
date: 2013-08-13 10:35:56.000000000 +08:00
type: post
published: true
status: publish
categories: database
---
It happen when i have a code like below

	function connect()
	{
		return sqlsrv_connect(..);
	}
	..

	$result = sqlsrv_query(connect(), $sql);  


The error mysteriously went away when i change the code to this

	$connect = connect();
	$result  = sqlsrv_query($connect, $sql);
