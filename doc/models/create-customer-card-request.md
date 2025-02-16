
# Create Customer Card Request

Defines the fields that are included in the request body of a request
to the `CreateCustomerCard` endpoint.

## Structure

`Create Customer Card Request`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `card_nonce` | `string` | Required | A card nonce representing the credit card to link to the customer.<br><br>Card nonces are generated by the Square payment form when customers enter<br>their card information. For more information, see<br>[Walkthrough: Integrate Square Payments in a Website](https://developer.squareup.com/docs/web-payments/take-card-payment).<br><br>__NOTE:__ Card nonces generated by digital wallets (such as Apple Pay)<br>cannot be used to create a customer card. |
| `billing_address` | [`Address`](../../doc/models/address.md) | Optional | Represents a postal address in a country.<br>For more information, see [Working with Addresses](https://developer.squareup.com/docs/build-basics/working-with-addresses). |
| `cardholder_name` | `string` | Optional | The full name printed on the credit card. |
| `verification_token` | `string` | Optional | An identifying token generated by [Payments.verifyBuyer()](https://developer.squareup.com/reference/sdks/web/payments/objects/Payments#Payments.verifyBuyer).<br>Verification tokens encapsulate customer device information and 3-D Secure<br>challenge results to indicate that Square has verified the buyer identity. |

## Example (as JSON)

```json
{
  "billing_address": {
    "address_line_1": "500 Electric Ave",
    "address_line_2": "Suite 600",
    "administrative_district_level_1": "NY",
    "country": "US",
    "locality": "New York",
    "postal_code": "10003"
  },
  "card_nonce": "YOUR_CARD_NONCE",
  "cardholder_name": "Amelia Earhart"
}
```

