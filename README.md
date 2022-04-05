# COMP-3040 API Specifications Assignment

## MB Parks API

MB Parks is a free API that will provide detailed information on campsites in parks based on specified **size**, **availability**, and **electrical offerings** of the site. The API will gather campsites around Manitoba that match the desired specifications and respond with the list containing further details about each individual site.

Please refer to the documentation below to see how to implement the MB Parks API.

## Endpoints & Parameters
`GET  http://www.mbparks.com/campsites`
Returns a list of campsites in Manitoba that match the given query parameters (see below).

### Parameters
* park_name (string): Full name of the park. Optional.
* bay_name (string): Full name of the bay the park is nearest to, if applicable. Optional
* lot_number (int): Number of the particular lot in the park, if applicable. Optional.
* availability (boolean): Availability of the lot number specified and in the park specified, if applicable. Optional.
* tree_coverage (string): Description of tree coverage for a particular lot number, if applicable. Optional.
* size (string): Size of the particular lot chosen, if applicable. Optional.
* electrical (boolean): Availablity of electrical outlets in the particular lot specified, if applicable. Optional.

## Resources

```json
{
"resources": [
		{
			"endpoint": "http://www.mbparks.com/campsites",
			"returns": "a list of camp sites in Manitoba"
		},
		{
			"endpoint": "http://www.mbparks.com/campsites?size=large&available=true&electrical=true",
			"returns": "a list of large available camp sites in Manitoba with electricity"
		}
	],
	"status": "OK"
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
