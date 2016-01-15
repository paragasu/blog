---
layout: post  
title: "PostgreSQL ENUM type"
date: 2016-01-15 15:10:00 +0800  
categories: database
---
To create enum type

   CREATE TYPE colors AS ENUM ('grey', 'skyblue', 'black');  

To list enum values

	SELECT ENUM_RANGE(null::colors); or  
	SELECT UNNEST(ENUM_RANGE(null::colors)) AS colors;  

To add new item on the enum list

	ALTER TYPE colors ADD VALUE 'orange' AFTER 'skyblue';

To delete item from enum list

	ALTER TYPE colors DROP attribute 'orange';

To drop enum type

	DROP type colors


There is a more elegant way using domain to enforce value from [David E. Wheeler post](http://justatheory.com/computers/databases/postgresql/enforce-set-of-values.html)  

	CREATE DOMAIN eye_color AS TEXT
	CONSTRAINT valid_eye_colors CHECK (
		VALUE IN ( 'blue', 'green', 'brown' )
	);

	CREATE TABLE faces (
		face_id SERIAL PRIMARY KEY,
		name TEXT NOT NULL DEFAULT '',
		eye_color eye_color NOT NULL
	);


Related  
[Enum support function](http://www.postgresql.org/docs/current/static/functions-enum.html)  
[Alter type](http://www.postgresql.org/docs/current/static/sql-altertype.html)  
[Enforce set of values](http://justatheory.com/computers/databases/postgresql/enforce-set-of-values.html)  
	

	

