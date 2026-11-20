# ViewsApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**recordComicView**](ViewsApi.md#recordcomicviewoperation) | **POST** /view | Record comic/chapter view |



## recordComicView

> RecordComicView200Response recordComicView(recordComicViewRequest)

Record comic/chapter view

Logs a view data point into Cloudflare Analytics Engine dataset.

### Example

```ts
import {
  Configuration,
  ViewsApi,
} from '@komikhq/komikhq-typescript';
import type { RecordComicViewOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new ViewsApi();

  const body = {
    // RecordComicViewRequest
    recordComicViewRequest: ...,
  } satisfies RecordComicViewOperationRequest;

  try {
    const data = await api.recordComicView(body);
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
| **recordComicViewRequest** | [RecordComicViewRequest](RecordComicViewRequest.md) |  | |

### Return type

[**RecordComicView200Response**](RecordComicView200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | View recorded successfully. |  -  |
| **400** | Invalid payload. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

