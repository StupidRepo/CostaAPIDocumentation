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
| `cardNumber` | This is the card number you may see on the *physical* card, and is also the number that the QR code is generated from. |
| `givexNumber` | givex internal number. May be related to [`givex.com`](https://web.givex.com/). |
| `status` | The status of this card. Most likely `active`. |
| `description` | Description of what this card is for. Usually `Costa Pay`. Afaik, Costa Pay isn't used. |
| `currency` | Card currency. `GBP`, `USD`, etc. |
| `certificateBalance` | TBR. |
| `pointsBalance` | Amount of points (a.k.a beans) on the card. As of June 2024, the maximum is `10` before it resets to `0`. *Did you know?: The maximum has changed multiple times, going from `6` to `8` and now `10`.* |
| `pointsValue*` | How much the points are worth in the currency of the card. |
| `type` | The type of this card. Costa started switching to digital cards instead of physical sometime around 2022/2023, so this is usually `digital`. |
| `preferred` | Whether or not this is the preferred card on the account. Most likely `true`. |
| `groups` | TBR. |
| `loyaltyScheme` | TBR. Most likely ` `. |
| `beansSequence` | Each type of bean collected towards your free drink. |
| `isBeansEnabled` | Most likely `true` unless you've been f*cking about with their systems and have (*ahem*) BEAN restricted. Ha... ha... |
| `permission*` | Self-explanatory. |
*Most of this section has yet TBR & TBW.*