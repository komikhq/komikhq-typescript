# SystemApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**clearSystemCache**](SystemApi.md#clearsystemcache) | **POST** /admin/system/clear-cache | Clear search cache (Admin only) |
| [**getSystemStatus**](SystemApi.md#getsystemstatus) | **GET** /admin/system/status | System infrastructure status (Admin only) |
| [**purgeSystemStorage**](SystemApi.md#purgesystemstorage) | **POST** /admin/system/purge-storage | Purge orphan files from R2 storage (Admin only) |
| [**syncSystemViews**](SystemApi.md#syncsystemviews) | **POST** /admin/system/sync-views | Manually trigger view sync and rankings refresh (Admin only) |



## clearSystemCache

> ClearSystemCache200Response clearSystemCache()

Clear search cache (Admin only)

Invalidate all cached search suggestions stored in Cloudflare KV.

### Example

```ts
import {
  Configuration,
  SystemApi,
} from '@komikhq/komikhq-typescript';
import type { ClearSystemCacheRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new SystemApi(config);

  try {
    const data = await api.clearSystemCache();
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

[**ClearSystemCache200Response**](ClearSystemCache200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Cache cleared successfully |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getSystemStatus

> GetSystemStatus200Response getSystemStatus()

System infrastructure status (Admin only)

Inspect Cloudflare KV, R2, and Durable Objects connectivity status.

### Example

```ts
import {
  Configuration,
  SystemApi,
} from '@komikhq/komikhq-typescript';
import type { GetSystemStatusRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new SystemApi(config);

  try {
    const data = await api.getSystemStatus();
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

[**GetSystemStatus200Response**](GetSystemStatus200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | System infrastructure diagnostic report |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## purgeSystemStorage

> PurgeSystemStorage200Response purgeSystemStorage()

Purge orphan files from R2 storage (Admin only)

Scan R2 bucket and delete orphaned files not associated with any comic or user.

### Example

```ts
import {
  Configuration,
  SystemApi,
} from '@komikhq/komikhq-typescript';
import type { PurgeSystemStorageRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new SystemApi(config);

  try {
    const data = await api.purgeSystemStorage();
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

[**PurgeSystemStorage200Response**](PurgeSystemStorage200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Storage purge operation completed |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## syncSystemViews

> SyncSystemViews200Response syncSystemViews()

Manually trigger view sync and rankings refresh (Admin only)

Execute background tasks to sync comic view deltas from KV to DB and refresh rankings.

### Example

```ts
import {
  Configuration,
  SystemApi,
} from '@komikhq/komikhq-typescript';
import type { SyncSystemViewsRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new SystemApi(config);

  try {
    const data = await api.syncSystemViews();
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

[**SyncSystemViews200Response**](SyncSystemViews200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Task executed successfully |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |
| **500** | Task execution failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

