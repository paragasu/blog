---
layout: post
title: Calculate distance between two point on earth in PostgreSQL
date: 2015-10-29 02:54:15.000000000 +08:00
type: post
published: true
status: publish
categories:
- database
tags:
- calculate distance
- postgresql
meta:
  sharing_disabled: '1'
  _rest_api_published: '1'
  _rest_api_client_id: "-1"
  _publicize_job_id: '16314458986'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
  first_name: ''
  last_name: ''
---
Come across nice function by Merlin Moncure posted on grokbase.


	CREATE OR REPLACE 
	FUNCTION calculate_distance(lat1 float8, lon1 float8, lat2 float8, lon2 float8)
	RETURNS float8 AS
	$$
		SELECT ACOS(SIN(RADIANS($1)) * SIN(RADIANS($3)) 
			 + COS(RADIANS($1)) * COS(RADIANS($3)) 
			 * COS(RADIANS($4) - RADIANS($2))) * 6371;

	$$ LANGUAGE 'sql' IMMUTABLE;


More details  
[Calculating distance between longitude and latitude](http://grokbase.com/t/postgresql/pgsql-general/1069rn3ca0/calculating-distance-between-longitude-and-latitude)  
[Calculate distance, bearing and more](http://www.movable-type.co.uk/scripts/latlong.html)
