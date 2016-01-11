---
layout: post  
title: "Nodemon failed to start process, possible issue with exec arguments"  
date: 2016-01-11 11:27:00 +0800  
categories: nodejs  
---
Nodemon will crashed with this error when the exec comman return error code 2 


	[Nodemon] failed to start process, possible issue with exec arguments
	events.js:146
		throw err;
		^

	Error: Uncaught, unspecified "error" event. (2)
		at emit (events.js:144:17)

Error code 2 is reserved for bash. Command line tools like mocha or jshint sometimes will throw error 2.
When jshint or mocha executed as argument to -x in nodemon. Nodemon crash.

A simple workaround is to put exit 1 in the -x 

	$nodemon --e js -w ./ -d 1 -x 'mocha ./test || exit 1'


Related  
[Nodemon code](https://github.com/remy/nodemon/blob/e177dd7865376876b01c8c4b069bf21aaf75cf50/lib/monitor/run.js#L118)  
[JSHint integration on github](https://github.com/remy/nodemon/issues/627)  
[Nodejs exit code](https://github.com/nodejs/node-v0.x-archive/blob/master/doc/api/process.markdown#exit-codes)

