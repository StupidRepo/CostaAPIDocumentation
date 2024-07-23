# StatusType
Used to indicate status of a voucher.

## Values
| Value          | Code name      | Description                            |
| -------------- | -------------- | -------------------------------------- |
| `E`            | `EXPIRED`      | Expired voucher.                       |
| `I`            | `ISSUED`       | Voucher issues.                        |
| `U`            | `USED`         | Voucher is used.                       |
| `C`            | `CANCELLED`    | Cancelled. Unusable.                   |
| `S`            | `GIFTING_ONLY` | Not usable<sup>1</sup>, only giftable. |
| Anything else. | `UNKNOWN`      | Unknown status, time to freak out!!!   |

<sup>1</sup> May be useable, however I am unsure.

## Source
Class `VoucherResponseMapper` in Costa APK.

![Image source.](/images/types/StatusType.png)
![Image source.](/images/types/StatusType2.png)