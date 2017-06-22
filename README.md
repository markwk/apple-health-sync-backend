# API Server for Handling Apple Health Sync

NOTE: This project is a clone of https://github.com/MaximeHeckel/health-dashboard/tree/master/go/src/server

## Description: 

This is a Backend Server (in go lang) for handling a daily sync of Apple Health data and database storage in MongoDB

## Current Calls

* /api/v1/status => checks server availability status
* /api/v1/healthhook => endpoint for syncing data
* /api/v1/health/graphql 

## Configuration 

* Database Reference can be configured in /utils/utils.go
* Port Number is set in main.go

## Installation and Setup

* Install MongoDB and create a database. 
* Run MongoDB. 
* Install Go Lang and Sets GOPATHS.
* Install Govendor. 
* If running locally, set mongoDB reference in /utils/utils.go to MONGOCLIENTADDRESS = "mongodb://localhost:27017/YOUR-DATABASE-NAME"
* Run the command $ go get github.com/apple-health-sync-backend (This should install your backend in GOPATH/src/github.com/markwk)

After that, you should be able to go into your project directory in go and run $ go run main.go. You can test by going to localhost:8000/api/v1/status 
