# MongoDB
## Installation

I installed MongoDB Community 7 with Homebrew following this link: [mongoDB](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-os-x/#install-mongodb-community-edition)

Changed the storage path and log path in the `.config` file

#### To run MongoDB (i.e. the [`mongod`](https://www.mongodb.com/docs/manual/reference/program/mongod/#mongodb-binary-bin.mongod) process) **as a macOS service**, run:

```
sudo brew services start mongodb-community@7.0
```
- normally you don't need `sudo` but i need it somehow

#### To stop a [`mongod`](https://www.mongodb.com/docs/manual/reference/program/mongod/#mongodb-binary-bin.mongod) running as a macOS service, use the following command as needed:

```
sudo brew services stop mongodb-community@7.0
```


### mongod.conf file content
```
systemLog:
  destination: file
  path: /usr/local/var/log/mongodb/mongo.log
  logAppend: true
storage:
  dbPath: /usr/local/var/mongodb
net:
  bindIp: 127.0.0.1, ::1
  ipv6: true
```
### Install the dependencies
type this command in the folder where the package.JSON is
```
npm install
```

### run the server
```
npm run start
```

Webiste will run on 
http://localhost:5555/

### Situation where local host is occupied
- google kill local host

# Postman
## Create new url post and request
press button `+`

## Get new item
Press button `body` then `raw` and `send`

# Pages
## /
## /items
### get
- show all items
### post
- create new item (in postman for now cuz there's no UI)
## /items/:id
- get one itme
