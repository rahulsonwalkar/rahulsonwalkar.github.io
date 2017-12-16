# Smartcar API Documentaion

A live version of this API can be found on 

``` https://SmartcarIntern.herokuapp.com ```

Contents: 

[1. Getting started: Running locally](#getting-started-running-server-locally)

[2. API Endpoints](#api-endpoints)


## Getting started: Running server locally

Clone the repo:
```
$ git clone https://github.com/rahulsonwalkar/smartcar
```

Install dependencies & start:
```
$ cd smartcar
$ npm install
$ npm start       # Creates server on Localhost Port 3000
```

Tests:
Open a **new terminal window** (because local server needs to be running) to run tests
```
$ npm test        # Runs API tests on local server
```


## API Endpoints

Available IDs: **1234, 1235**

#### 1. Vehicle Info

  Request: 
  
  ` GET /vehicles/:id`

  Response:
  ```
  {
  "vin": "1213231",
  "color": "Metallic Silver",
  "doorCount": 4,
  "driveTrain": "v8"
  }
  ```
  Manual cURL request:
  ```
  curl https://SmartcarIntern.herokuapp.com/vehicles/1234 -X GET
  ```

#### 2. Security
   
  Request: 
  
  ` GET /vehicles/:id/doors`

  Response:
  ```
  [
  {"location":"backRight","locked":"True"},
  {"location":"frontRight","locked":"True"},
  {"location":"frontLeft","locked":"True"},
  {"location":"backLeft","locked":"False"}
  ]
  ```
  Manual cURL request:
  ```
  curl https://SmartcarIntern.herokuapp.com/vehicles/1234/doors -X GET
  ```
  
#### 3. Fuel Range

  Request: 
  
  ` GET /vehicles/:id/fuel`

  Response:
  ```
  {"percent":"12.1"}
  ```
  Manual cURL request:
  ```
  curl https://SmartcarIntern.herokuapp.com/vehicles/1234/fuel -X GET
  ```
  
#### 4. Battery Range

  Request: 
  
  ` GET /vehicles/:id/battery`

  Response:
  ```
  {"percent":"12.1"}
  ```
  Manual cURL request:
  ```
  curl https://SmartcarIntern.herokuapp.com/vehicles/1234/battery -X GET
  ```
  
#### 5. Engine (START & STOP)

  Request: 
  
  ` POST /vehicles/:id/engine`
  
  ```
  {
    "action" : "START | STOP"
  }
  ```
  Response:
  ```
  {"status":"sucess | error"}
  ```
  Manual cURL request:
  ```
  curl https://SmartcarIntern.herokuapp.com/vehicles/1234/engine -X POST -H 'Content-Type: application/json' -d '{"action": "START"}'
  ```
