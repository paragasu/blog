---
layout: post
title: "Https on Nodejs"  
data: 2016-01-28 16:02:00 +0800   
categories: nodejs  
---

	const https = require('https');
	const fs = require('fs');

	const options = {
	  key: fs.readFileSync('test/fixtures/keys/agent2-key.pem'),
	  cert: fs.readFileSync('test/fixtures/keys/agent2-cert.pem')
	};

	https.createServer(options, (req, res) => {
	  res.writeHead(200);
	  res.end('hello world\n');
	}).listen(8000);


Related  
[Nodejs doc](https://nodejs.org/api/https.html)


