# API for Finding COVID-19 Test Centers in Manitoba

This API provides the information of the test centers where any individual can go and test if they have already been infected with COVID. If a postal code is given, it can also show the nearest test center from that postal code.

## List of Endpoints with Parameters

This is a simple REST API with one endpoint which can which we can access using a GET request.

 ### Parameters

* **postalCode**(*string*) : postal code of an area to find the nearest COVID test center. REQUIRED

* **city**(*string*) : any city in Manitoba province.

* **testCenter**(*string*) : information of the given test center.

## Description of resources : 

### Resources :

```json
{
	"result" :
	{
		"test_center",
		"city",
		"opening_time",
		"closing_time",
		"availabilty"
	}
}
```

