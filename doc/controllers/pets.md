# Pets

the pet grouping

```ts
const petsController = new PetsController(client);
```

## Class Name

`PetsController`

## Methods

* [Create Pets](../../doc/controllers/pets.md#create-pets)
* [List Pets](../../doc/controllers/pets.md#list-pets)
* [Show Pet by Id](../../doc/controllers/pets.md#show-pet-by-id)


# Create Pets

Create a pet and key characteristics

```ts
async createPets(
  body: Pet,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Pet`](../../doc/models/pet.md) | Body, Required | A single Pet object used to create a new Pet |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

`void`

## Example Usage

```ts
const body: Pet = {
  name: 'Indiana',
  id: BigInt(12345),
};

try {
  // @ts-expect-error: unused variables
  // eslint-disable-next-line @typescript-eslint/no-unused-vars
  const { result, ...httpResponse } = await petsController.createPets(body);
  // Get more response info...
  // const { statusCode, headers } = httpResponse;
} catch (error) {
  if (error instanceof ApiError) {
    // @ts-expect-error: unused variables
    // eslint-disable-next-line @typescript-eslint/no-unused-vars
    const errors = error.result;
    // const { statusCode, headers } = error;
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | unexpected error | [`CustomError`](../../doc/models/custom-error.md) |


# List Pets

List all pets

```ts
async listPets(
  limit?: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<Pet[]>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `number \| undefined` | Query, Optional | How many items to return at one time (max 100)<br>**Constraints**: `<= 100` |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

[`Pet[]`](../../doc/models/pet.md)

## Example Usage

```ts
const limit = 10;

try {
  // @ts-expect-error: unused variables
  // eslint-disable-next-line @typescript-eslint/no-unused-vars
  const { result, ...httpResponse } = await petsController.listPets(limit);
  // Get more response info...
  // const { statusCode, headers } = httpResponse;
} catch (error) {
  if (error instanceof ApiError) {
    // @ts-expect-error: unused variables
    // eslint-disable-next-line @typescript-eslint/no-unused-vars
    const errors = error.result;
    // const { statusCode, headers } = error;
  }
}
```

## Example Response *(as JSON)*

```json
[
  {
    "id": 12345,
    "name": "Indiana",
    "petType": "dog"
  },
  {
    "id": 56789,
    "name": "Shadow",
    "petType": "cat"
  }
]
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | unexpected error | [`CustomError`](../../doc/models/custom-error.md) |


# Show Pet by Id

Info for a specific pet

```ts
async showPetById(
  petId: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<Pet>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `petId` | `string` | Template, Required | The id of the pet to retrieve |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

[`Pet`](../../doc/models/pet.md)

## Example Usage

```ts
const petId = '33918';

try {
  // @ts-expect-error: unused variables
  // eslint-disable-next-line @typescript-eslint/no-unused-vars
  const { result, ...httpResponse } = await petsController.showPetById(petId);
  // Get more response info...
  // const { statusCode, headers } = httpResponse;
} catch (error) {
  if (error instanceof ApiError) {
    // @ts-expect-error: unused variables
    // eslint-disable-next-line @typescript-eslint/no-unused-vars
    const errors = error.result;
    // const { statusCode, headers } = error;
  }
}
```

## Example Response *(as JSON)*

```json
{
  "id": 12345,
  "name": "Cody",
  "petType": "dog"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | unexpected error | [`CustomError`](../../doc/models/custom-error.md) |

