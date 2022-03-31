# COMP-3040 API Specifications Assignment


## Response

`GET http://www.mbparks.com/campsites?size=large&available=true&electrical=true`

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
