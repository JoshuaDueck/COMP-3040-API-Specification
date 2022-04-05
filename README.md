# COMP-3040 API Specifications Assignment

## MB Parks API

MB Parks is a free API that will provide detailed information on Manitoba parks, and provides a simple way to query campsites in Manitoba parks based on specified **size**, **availability**, **tree coverage** and **electrical offerings** of the site. The API will gather campsites around Manitoba that match the desired specifications and respond with the list containing further details about each individual site.

Please refer to the documentation below to see how to implement the MB Parks API.

### Endpoints
`http://www.mbparks.com/campsites`
* Returns a list of campsites in Manitoba that match the given query parameters (see below).

### Parameters
* `availability` (boolean): Availability of the lot number specified and in the park specified, if applicable. Optional.
* `tree_coverage` (string): Description of tree coverage for a particular lot number, if applicable. Optional.
* `size` (string): Size of the particular lot chosen, if applicable. Optional.
* `electrical` (boolean): Availablity of electrical outlets in the particular lot specified, if applicable. Optional.

### Resources

#### Results
```json
{
    "results": "A list of campsite objects."
}
```

#### Campsite
```json
{
    "park_name": "The official name of the park in Manitoba.",
    "bay_name": "The park-specific name of the bay containing this campsite.",
    "lot_number": "An integer representing the number of the lot within the bay.",
    "available": "A boolean value representing whether the lot is available.",
    "tree_coverage": "A string representing how many trees are surrounding the lot (none, low, medium, high).",
    "size": "A string representing the size of the lot (small, medium, large).",
    "electrical": "A boolean value representing whether the lot has electrical outlets."
}
```

## Sample Request & Response

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

## Authors

- Arjun Kaushal
- Braden Jonsson
- Winson Lam
- Joshua Dueck
- Anas Ashfaq Mehar
