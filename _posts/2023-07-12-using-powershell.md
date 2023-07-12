
---
title:  bicep using powershell
author: Atul Sahu
date: 2023-07-12 14:46:00 +0000
categories: [Blogging, Azure, Powershell]
tags: [getting started]
math: true
---

## Query

## Solution

Create two files, as below and run 

- TSQL query file
- Powershell 

I saved below Scriptfile ona local path `'..\Select.sql'`

```powershell

DECLARE @SqlCmd VARCHAR(4096);
BEGIN
	SET @SqlCmd = 'SELECT TOP(2) * FROM [dbo].[Employee]';
	PRINT @SQlCmd
	EXEC (@SQlCmd)
END

```

and powershell

```terminal

#region Connect to Azure SQL DB using Service Principal Account 
$TenantId = "XXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX"
$ServicePrincipalApplicationId = "XXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX"
$SqlServerName = "<Sql Server Name>"
$DatabaseName = '<DatabaseName>'
$clientsecret= "<secret in plain text>"
$ScriptFile = '..\Select.sql'

```

## Sample Output

>**Disclaimer**: This is a personal weblog. The opinions expressed here represent my own and not those of any entity with which I have been, am now, or will be affiliated.
