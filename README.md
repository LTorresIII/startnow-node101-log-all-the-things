*Log All The Things*

Description-
	This project will involve using node to build a logger.
	In this project you will build your own custom logger that will log some information about each request it recieves. 
	You will also expose an endpoint on the server so it would be easy for anyone to retieve the latest log data from the web. 

Instructions-
	Using express, implement a web server that saves data about each incoming request in a file called log.csv. Use csv file format with the following headers row:
	Agent
	Time
	Method
	Resource
	Version
	Status
	Start by creating a file called log.csv and add the following line of text:
	Agent,Time,Method,Resource,Version,Status
	Write the code required to generate a log line for every request following this format:
	Agent - the user-agent found in the request's header. You may find it helpful to reformat this (some user-agent strings may contain commas)
	Time - use the ISO date standard
	Method - one of the following methods: GET, POST, DELETE, etc.
	Resource - the path and the file requested
	Version - the http version of the request, check the request object for this value and be prepared to format the string
	Status - a number that is most likely 200, 404, or 500

	Every request to your server must be logged to the console
	Every request to your server must be logged to a file
	The log file is named log.csv and must be csv format
	Must use fs.appendFile, do not use fs.appendFileSync
	Expose an endpoint (does not require authentication) http://localhost:3000/logs that will return a json object with all the logs