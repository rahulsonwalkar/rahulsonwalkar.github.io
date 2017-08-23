# Rechat API

## Prerequisites

```bash
Git
Node.js version v8.x.x
Postgres
```
## Getting started

#### Clone the repository

```bash
git clone git@bitbucket.org:rechat/server.git
cd shortlisted-server
```

#### Install the dependencies

```bash
npm install
```
#### Import schema into your database
```bash
psql rechat < lib/data/schema.sql
```

#### Set configuration options of your database

```bash
vim lib/config.js
```
And set configuration options of your database.

## Run the app
```bash
npm start
```
listening at port 3078

## Howto Test

```bash
npm test
```
