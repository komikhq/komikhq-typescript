# GenresApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listGenres**](GenresApi.md#listgenres) | **GET** /genres | List all comic genres |



## listGenres

> ListGenres200Response listGenres()

List all comic genres

Returns the full catalog of available comic genres.

### Example

```ts
import {
  Configuration,
  GenresApi,
} from '@komikhq/komikhq-typescript';
import type { ListGenresRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new GenresApi();

  try {
    const data = await api.listGenres();
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

[**ListGenres200Response**](ListGenres200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Genre catalog list. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

