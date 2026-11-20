# HealthApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getHealthStatus**](HealthApi.md#gethealthstatus) | **GET** /health | Service health and runtime environment check |



## getHealthStatus

> GetHealthStatus200Response getHealthStatus()

Service health and runtime environment check

Returns database latency, Node.js runtime compatibility, and Cloudflare resource binding connectivity status.

### Example

```ts
import {
  Configuration,
  HealthApi,
} from '@komikhq/komikhq-typescript';
import type { GetHealthStatusRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new HealthApi();

  try {
    const data = await api.getHealthStatus();
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

[**GetHealthStatus200Response**](GetHealthStatus200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Health and environment diagnostic details. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

