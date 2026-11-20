# AppRoutesApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**viewsPost**](AppRoutesApi.md#viewspost) | **POST** /views |  |



## viewsPost

> viewsPost()



### Example

```ts
import {
  Configuration,
  AppRoutesApi,
} from '@komikhq/komikhq-typescript';
import type { ViewsPostRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new AppRoutesApi();

  try {
    const data = await api.viewsPost();
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

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

