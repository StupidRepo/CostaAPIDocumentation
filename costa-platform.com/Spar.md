# Spar
| URL(s) | Method(s) | Authorization Required? |
| ------ | --------- | ----------------------- |
| `https://costa-platform.com/spar` | `POST` | `No` |

## Description
Used for the in-app Costa Coffee locator, where it shows a map of nearby Costa Coffee stores (or Costa Express machines). This endpoint returns the longitude, latitude and other details about each Costa location that is close around the provided longitude and latitude that is sent in body parameters.

*Note: This is low-priority due to the fact that most of it is self-explanatory and is going to take at least an hour for me to document.*

*This section has yet TBR & yet TBW.*

## Body Parameters
- Type: `application/json`

## Example Response
- Status Code: 200
```json
{
	"data": {
		"sites": {
			"items": [{

            }]
        }
    }
}
```

*This section has yet TBR & yet TBW.*