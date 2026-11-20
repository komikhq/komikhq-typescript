# ReadingHistoryApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteReadingHistory**](ReadingHistoryApi.md#deletereadinghistory) | **DELETE** /history/{comicId} | Clear reading history for comic |
| [**listReadingHistory**](ReadingHistoryApi.md#listreadinghistory) | **GET** /history | List user reading history |
| [**recordReadingHistory**](ReadingHistoryApi.md#recordreadinghistoryoperation) | **POST** /history | Record chapter reading progress |



## deleteReadingHistory

> SuccessResponse deleteReadingHistory(comicId)

Clear reading history for comic

Removes reading history records for a specific comic.

### Example

```ts
import {
  Configuration,
  ReadingHistoryApi,
} from '@komikhq/komikhq-typescript';
import type { DeleteReadingHistoryRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ReadingHistoryApi(config);

  const body = {
    // string | Comic ID
    comicId: comicId_example,
  } satisfies DeleteReadingHistoryRequest;

  try {
    const data = await api.deleteReadingHistory(body);
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

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reading history deleted successfully. |  -  |
| **401** | Unauthorized. |  -  |
| **404** | Not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listReadingHistory

> ListReadingHistory200Response listReadingHistory()

List user reading history

Returns reading history entries and chapter progress for the authenticated user.

### Example

```ts
import {
  Configuration,
  ReadingHistoryApi,
} from '@komikhq/komikhq-typescript';
import type { ListReadingHistoryRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ReadingHistoryApi(config);

  try {
    const data = await api.listReadingHistory();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ListReadingHistory200Response**](ListReadingHistory200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reading history list. |  -  |
| **401** | Unauthorized. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## recordReadingHistory

> RecordReadingHistory200Response recordReadingHistory(recordReadingHistoryRequest)

Record chapter reading progress

Saves or updates reading progress, last read page, and completion status for a comic chapter.

### Example

```ts
import {
  Configuration,
  ReadingHistoryApi,
} from '@komikhq/komikhq-typescript';
import type { RecordReadingHistoryOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ReadingHistoryApi(config);

  const body = {
    // RecordReadingHistoryRequest
    recordReadingHistoryRequest: ...,
  } satisfies RecordReadingHistoryOperationRequest;

  try {
    const data = await api.recordReadingHistory(body);
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
| **recordReadingHistoryRequest** | [RecordReadingHistoryRequest](RecordReadingHistoryRequest.md) |  | |

### Return type

[**RecordReadingHistory200Response**](RecordReadingHistory200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reading progress recorded successfully. |  -  |
| **400** | Invalid payload. |  -  |
| **401** | Unauthorized. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

