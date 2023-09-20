
# Getting Started with Petstore

## Introduction

The API enables users to view detailed information about a specific pet store and its available pets. The API can be used by pet owners, pet adoption agencies, and anyone looking for information about pets in a particular area.

## Install the Package

Run the following command from your project directory to install the package from npm:

```ts
npm install tahiratesttypescript2@1.0.8
```

For additional package details, see the [Npm page for the tahiratesttypescript2@1.0.8  npm](https://www.npmjs.com/package/tahiratesttypescript2/v/1.0.8).

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/TahiraKhattak/typescript_demo/tree/1.0.8/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| `timeout` | `number` | Timeout for API calls.<br>*Default*: `0` |
| `httpClientOptions` | `Partial<HttpClientOptions>` | Stable configurable http client options. |
| `unstableHttpClientOptions` | `any` | Unstable configurable http client options. |
| `accessToken` | `string` | The OAuth 2.0 Access Token to use for API requests. |

### HttpClientOptions

| Parameter | Type | Description |
|  --- | --- | --- |
| `timeout` | `number` | Timeout in milliseconds. |
| `httpAgent` | `any` | Custom http agent to be used when performing http requests. |
| `httpsAgent` | `any` | Custom https agent to be used when performing http requests. |
| `retryConfig` | `Partial<RetryConfiguration>` | Configurations to retry requests. |

### RetryConfiguration

| Parameter | Type | Description |
|  --- | --- | --- |
| `maxNumberOfRetries` | `number` | Maximum number of retries. <br> *Default*: `0` |
| `retryOnTimeout` | `boolean` | Whether to retry on request timeout. <br> *Default*: `true` |
| `retryInterval` | `number` | Interval before next retry. Used in calculation of wait time for next request in case of failure. <br> *Default*: `1` |
| `maximumRetryWaitTime` | `number` | Overall wait time for the requests getting retried. <br> *Default*: `0` |
| `backoffFactor` | `number` | Used in calculation of wait time for next request in case of failure. <br> *Default*: `2` |
| `httpStatusCodesToRetry` | `number[]` | Http status codes to retry against. <br> *Default*: `[408, 413, 429, 500, 502, 503, 504, 521, 522, 524]` |
| `httpMethodsToRetry` | `HttpMethod[]` | Http methods to retry against. <br> *Default*: `['GET', 'PUT']` |

The API client can be initialized as follows:

```ts
const client = new Client({
  timeout: 0,
  accessToken: 'AccessToken',
});
```

## Authorization

This API uses `OAuth 2 Bearer token`.

## List of APIs

* [Pets](https://www.github.com/TahiraKhattak/typescript_demo/tree/1.0.8/doc/controllers/pets.md)

## Classes Documentation

* [ApiResponse](https://www.github.com/TahiraKhattak/typescript_demo/tree/1.0.8/doc/api-response.md)
* [ApiError](https://www.github.com/TahiraKhattak/typescript_demo/tree/1.0.8/doc/api-error.md)

