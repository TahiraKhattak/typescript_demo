
# Custom Error

## Structure

`CustomError`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `number` | Required | the code associated with the error returned |
| `message` | `string` | Required | detailed message about the error returned |

## Example (as JSON)

```json
{
  "code": 101010,
  "message": "Invalid pet type, only cat and dogs allowed"
}
```

