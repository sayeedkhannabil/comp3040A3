# *API for Finding COVID-19 Test Centers in Manitoba*


> This API provides the information of the test centers where any individual can go and test if they have already been infected with COVID-19.
>
> One can get the name of the test centers, and their location, timing, availability for a given postal-code.
>
> Please note that this API is an open-source project. So, you do not need an API-Key to access this API. If you encounter any difficulties while using this API, feel free to contact us or create a GitHub issue. 

## *List of Endpoints with Parameters*


>### *Endpoints*
>
>> This is a simple REST API with one endpoint which can be accessed using a GET request to https://api.covid-test-site.org/json.
>
>### *Parameters*
> >* .**postalCode**(*string*) : postal code of an area to find the nearest COVID-19 test centers. Required.
> >* **city**(*string*) : name of any city in the province of Manitoba. Optional.
> >* **centerName**(*string*) : name of any known test center. Optional.

## *Description of resources :* 

>### *Resources* :
>``` json
>{
>"result":
>{
>	"test_center":"Victoria General Hospital",
>	"city":"Winnipeg",
>	"opening_time":"0800",
>	"closing_time":"2200",
>	"availabilty":"true"
>},
>"status":"OK"
>}
>```

>### *Description*
| Object         | Type   | Description                                       |
| -------------- | ------ | ------------------------------------------------- |
| `test_center`  | string | name of the test center                           |
| `city`         | string | name of the city                                  |
| `opening_time` | string | opening time of the test center                   |
| `closing_time` | string | closing time of the test center                   |
| `availabilty`  | bool   | shows if the test center is close due to outbreak |



## *Sample Request with Sample Response*

>* Sample request using **postalCode** parameter :
>```
>https://api.covid-test-site.org/json?postalCode="R3T2K1"
>```
>
>#### Response :
>``` json
>{
>"result":
>{
>	"test_center":"Main Street Drive-Thru COVID-19 Testing Site",
>	"city":"Winnipeg",
>	"opening_time":"0800",
>	"closing_time":"2200",
>	"availabilty":"true"
>},
>"status":"OK"
>}
>```

>* Sample request using **city** parameter :
>```
>https://api.covid-test-site.org/json?city="brandon"
>```
>#### Response :
>``` json
>{
>"result":
>{
>	"test_center":"Brandon Town COVID-19 Assessment Centre",
>	"city":"Brandon",
>	"opening_time":"0800",
>	"closing_time":"2200",
>	"availabilty":"true"
>},
>"status":"OK"
>}
>```

>* Sample request using **centerName** parameter :
>```
>https://api.covid-test-site.org/json?centerName="victoria general hospital"
>```
>#### Response :
>``` json
>{
>"result":
>{
>	"test_center":"Victoria General Hospital",
>	"city":"Winnipeg",
>	"opening_time":"0800",
>	"closing_time":"2200",
>	"availabilty":"true"
>},
>"status":"OK"
>}
>```
