# RatingsApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getComicRating**](RatingsApi.md#getcomicrating) | **GET** /ratings/{comicId} | Get comic rating stats and user rating |
| [**upsertComicRating**](RatingsApi.md#upsertcomicratingoperation) | **POST** /ratings | Rate a comic |



## getComicRating

> GetComicRating200Response getComicRating(comicId)

Get comic rating stats and user rating

Returns average rating score, total rating count, and user\&#39;s own score if authenticated.

### Example

```ts
import {
  Configuration,
  RatingsApi,
} from '@komikhq/komikhq-typescript';
import type { GetComicRatingRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new RatingsApi();

  const body = {
    // string | Comic ID
    comicId: comicId_example,
  } satisfies GetComicRatingRequest;

  try {
    const data = await api.getComicRating(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **comicId** | `string` | Comic ID | [Defaults to `undefined`] |

### Return type

[**GetComicRating200Response**](GetComicRating200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comic rating data. |  -  |
| **400** | Invalid comicId. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## upsertComicRating

> GetComicRating200Response upsertComicRating(upsertComicRatingRequest)

Rate a comic

Submits a rating score (1-10) and optional review text for a comic.

### Example

```ts
import {
  Configuration,
  RatingsApi,
} from '@komikhq/komikhq-typescript';
import type { UpsertComicRatingOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RatingsApi(config);

  const body = {
    // UpsertComicRatingRequest
    upsertComicRatingRequest: ...,
  } satisfies UpsertComicRatingOperationRequest;

  try {
    const data = await api.upsertComicRating(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **upsertComicRatingRequest** | [UpsertComicRatingRequest](UpsertComicRatingRequest.md) |  | |

### Return type

[**GetComicRating200Response**](GetComicRating200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rating submitted successfully. |  -  |
| **400** | Invalid payload. |  -  |
| **401** | Unauthorized. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

