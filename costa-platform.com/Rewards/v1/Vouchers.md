# Vouchers
| URL(s) | Method(s) | Authorization Required? |
| ------ | --------- | ----------------------- |
| `https://costa-platform.com/rewards/v1/vouchers?statuses&expiryDateFrom` | `GET` | `Yes` |

## Description
Rewards, like discounts and such. Some examples:
- `Free cookie when you buy a drink`
  - Do I need to explain?
- `£1 off food`
  - Take £1 off of any 1 food item on your next order.

## Query Paremeters
| Name | Description | Example |
| ---- | ----------- | ------- |
| `statuses` | Vouchers with one of these status types will be included | `S,I,E` |
| `expiryDateFrom` | Vouchers with an expiry date newer than `expiryDateFrom` will be included | `2024-05-28` |

## Example Response
- Status Code: 200

The response is an array of objects, where each object is a coupon/voucher. Look below the codeblock for details on the Coupon/Voucher object.

This has been heavily shortened for this example.
```json
[{
	"id": 000000000,
	"couponNumber": "XXXXXXXXXXXX",
	"expiryDate": "2024-06-04T22:59:59Z",
	"status": "E",
	"couponType": "U",
	"useQuantity": 1,
	"unlimitedUse": false,
	"optedIn": false,
	"discount": true,
	"discountType": "P",
	"discountValue": 100.0,
	"discountLevel": "P",
	"resourceId": "5Nc60QAQqkFUCys8E3q2me",
	"iconCategory": "coffee",
	"name": "Free cookie when you buy a drink",
	"category": "D",
	"channels": ["L", "X"],
	"subChannels": [],
	"shareable": false,
	"shared": false,
	"activeHours": "111111111111111111111111",
	"activeDays": "1111111"
}]
```
| Name | Description |
| ---- | ----------- |
| `id` | Internal ID for this coupon/voucher. |
| `couponNumber` | Internal number for this coupon/voucher. |
| `expiryDate` | ISO 8601 date of when this coupon/voucher is considered to be expired. |
| `status` | The status of this coupon. Can be one of the following: `E` for `Expired`, `I` for `Active`, or `S` for `TBR - Could mean 'Special'?` |
| `couponType` | TBR. Most likely `U`. |
| `useQuantity` | How many times this coupon/voucher can be used. |
| `unlimitedUse` | Whether or not this coupon/voucher can be infinitely used. |
| `optedIn` | Whether this award has been selected to be used in-store or in-app. |
| `discount` | Whether or not this coupon/voucher gives a discount |
| `discountType` | TBR. Possible values: `V`, `P`. |
| `discountValue` | Value of the discount. |
| `discountLevel` | TBR. Possible values: `C`, `P`. |
| `resourceId` | TBR. |
| `iconCategory` | Which icon to show. Possible values: `coffee`, `pound_discount`, `treat_drop`. |
| `name` | Name of this coupon/voucher, which is used & displayed in-app. |
| `category` | TBR. Most likely `D`. |
| `channels` | TBR. Most likely `["L", "X"]`. |
| `subChannels` | TBR. Most likely `[]`. |
| `shareable` | Whether or not you can share this coupon/voucher with another person who has a Costa membership card. |
| `shared` | Whether or not this has been shared to you by someone else. |
| `activeHours` | The length of this string represents how many hours of a day. For example, `111` = 3 hours. This will most likely be `111111111111111111111111` (24 hours). |
| `activeDays` | The length of this strings represents how many days of a wekk. For example, `111` = 3 days. This will most likely be `1111111` (7 days). |

*Most of this section has yet TBR & TBW.*