
# Pet

## Structure

`Pet`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | the name lovingly given to the pet |
| `type` | [`PetTypeEnum \| undefined`](../../doc/models/pet-type-enum.md) | Optional | the type of pets allowed |
| `id` | `bigint` | Required | a unique identifier for a Pet |

## Example (as JSON)

```json
{
  "name": "Fido",
  "id": 1234,
  "type": "dog"
}
```

