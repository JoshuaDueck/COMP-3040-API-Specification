# COMP-3040 API Specifications Assignment

## MB Parks API

MB Parks is a free API that will provide detailed information on campsites in parks based on specified **size**, **availability**, and **electricity** of the site. The API will gather campsites around Manitoba that match the desired specifications and respond with the list containing further details about each individual site.

Please check the documentation below to see how to implement the MB Parks API.

## Sample Request

`GET http://www.mbparks.com/campsites?size=large&available=true&electrical=true`

## Sample Response

```json
{
	"results": [
		{
			"park_name": "Birds' Hill Park",
			"bay_name": "Lark Bay",
			"lot_number": 1,
			"available": true,
			"tree_coverage": "medium",
			"size": "large",
			"electrical": true
		},
		{
			"park_name": "Birds' Hill Park",
			"bay_name": "Lark Bay",
			"lot_number": 2,
			"available": true,
			"tree_coverage": "medium",
			"size": "large",
			"electrical": true
		},
		{
			"park_name": "Birds' Hill Park",
			"bay_name": "Lark Bay",
			"lot_number": 3,
			"available": true,
			"tree_coverage": "medium",
			"size": "large",
			"electrical": true
		},
		{
			"park_name": "St. Malo",
			"bay_name": "Fox Bay",
			"lot_number": 1,
			"available": true,
			"tree_coverage": "high",
			"size": "large",
			"electrical": true
		}
	],
	"status": "OK"
}
```
