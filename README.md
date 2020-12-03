# API for Finding COVID-19 Test Centers in Manitoba

This API provides the information of the test centers where any individual can go and test if they have already been infected with COVID. If a postal code is given, it can also show the nearest test center from that postal code.

## List of Endpoints with Parameters

This is a simple REST API with one endpoint which can which we can access using a GET request to https://api.covid-test-site.org/json.

 ### Parameters

* **postalCode**(*string*) : postal code of an area to find the nearest COVID test center. REQUIRED

* **city**(*string*) : any city in Manitoba province.

* **testCenter**(*string*) : information of the given test center.

## Description of resources : 

### Resources :

``` json
{
	"result":
	{
		"test_center":"Victoria General Hospital",
		"city":"Winnipeg",
		"opening_time":"0800",
		"closing_time":"2200",
		"availabilty":"true"
	},
	"status":"OK"
}
```

### Description

|  Object       |  Type  |          Description                               |
|-------------- |--------|----------------------------------------------------|
| `test_center` | string | name of the test center                            |
| `city`        | string | name of the city                                   |
| `opening_time`| string | opening time of the test center                    |
| `closing_time`| string | closing time of the test center                    |
| `availabilty` | bool   | shows if the test center is close due to outbreak  |



## Sample Request with Sample Response

* Sample request using **postalCode** parameter :
```
https://api.covid-test-site.org/json?postalCode="r3t2k1"
```
#### Response :
``` json
{
	"result":
	{
		"test_center":"Victoria General Hospital",
		"city":"Winnipeg",
		"opening_time":"0800",
		"closing_time":"2200",
		"availabilty":"true"
	},
	"status":"OK"
}
```

* Sample request using **city** parameter :
```
https://api.covid-test-site.org/json?city="brandon"
```
#### Response :
``` json
{
	"result":
	{
		"test_center":"Victoria General Hospital",
		"city":"Winnipeg",
		"opening_time":"0800",
		"closing_time":"2200",
		"availabilty":"true"
	},
	"status":"OK"
}
```

* Sample request using **test_center** parameter :
```
https://api.covid-test-site.org/json?test_center="victorial general hospital"
```
#### Response :
``` json
{
	"result":
	{
		"test_center":"Victoria General Hospital",
		"city":"Winnipeg",
		"opening_time":"0800",
		"closing_time":"2200",
		"availabilty":"true"
	},
	"status":"OK"
}
```