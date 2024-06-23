# Cards
| URL(s) | Method(s) | Authorization Required? |
| ------ | --------- | ----------------------- |
| `https://costa-platform.com/loyalty/v2/cards/:id` | `GET` | `Yes` |


## Description
Fetch card details from an ID, for details such as:
- Card Number
- Points (a.k.a Beans) Balance
- Beans Sequence
### Bean Types
- `EXPRS_BEAN` - Express Bean - Beans rewarded from Costa Express machines commonly found at gas stations.
- `STAND_BEAN` - Standard Bean - Beans rewarded from scanning a membership card/QR code from within a dedicated Costa store.
- `TBR` - Referral Bean - Beans rewarded from referring someone else to the app.

## Path Parameters
### ID
The card/membership ID (i.e `633780XXXXXXXXXXXXXXXX`).

## Example Response
- Status Code: 200
```json
{
	"id": "633780XXXXXXXXXXXXXXXX",
	"cardISO": 633780,
	"serialNumber": 1111111111,
	"cardNumber": "633780XXXXXXXXXXXXXXXX",
	"givexNumber": "633780XXXXXXXXXXXXXXXX",
	"status": "active",
	"description": "Costa Pay",
	"currency": "GBP",
	"certificateBalance": 0.0,
	"pointsBalance": 7,
	"pointsValueGBP": 7,
	"type": "digital",
	"preferred": true,
	"groups": [],
	"loyaltyScheme": "",
	"beansSequence": ["EXPRS_BEAN", "EXPRS_BEAN", "EXPRS_BEAN", "STAND_BEAN", "STAND_BEAN", "STAND_BEAN", "STAND_BEAN"],
	"isBeansEnabled": true,
	"permissionSMS": false,
	"permissionEmail": true,
	"permissionPost": false,
	"permissionPhone": false,
	"permissionMobile": false,
	"permissionPush": false,
	"permissionTwitter": false,
	"permissionFacebook": false,
	"permissionSurvey": true,
	"permissionProfiling": true,
	"permissionAttr1": true,
	"permissionAttr2": true,
	"permissionAttr3": false,
	"permissionAttr4": false,
	"permissionAttr5": false,
	"permissionAttr6": false,
	"permissionAttr7": false,
	"permissionAttr8": false,
	"permissionAttr9": false,
	"permissionAttr10": false
}
```

| Name | Description |
| ---- | ----------- |
| `id` | The card's internal ID. |
| `cardISO` | The ISO type of the card. Usually just `633780`. |
| `serialNumber` | The SN of the card. |
| `cardNumber` | The card number you may see on the *physical* card and the one that the QR code is generated from. |
| `givexNumber` | givex internal number. May be related to [`givex.com`](https://web.givex.com/). |
| `status` | TBR. Most likely `active`. |

*This section has yet to be **fully** researched.*