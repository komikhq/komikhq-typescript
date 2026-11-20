# ModerationApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**adminListReports**](ModerationApi.md#adminlistreports) | **GET** /admin/reports | List user reports (Admin only) |
| [**adminUpdateReport**](ModerationApi.md#adminupdatereportoperation) | **PATCH** /admin/reports/{id} | Update report status (Admin only) |



## adminListReports

> AdminListReports200Response adminListReports(status)

List user reports (Admin only)

Fetch reported comments and issues filtered by status.

### Example

```ts
import {
  Configuration,
  ModerationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminListReportsRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ModerationApi(config);

  const body = {
    // 'PENDING' | 'RESOLVED' | 'REJECTED' | Report review status (optional)
    status: status_example,
  } satisfies AdminListReportsRequest;

  try {
    const data = await api.adminListReports(body);
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
| **status** | `PENDING`, `RESOLVED`, `REJECTED` | Report review status | [Optional] [Defaults to `&#39;PENDING&#39;`] [Enum: PENDING, RESOLVED, REJECTED] |

### Return type

[**AdminListReports200Response**](AdminListReports200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of reports |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminUpdateReport

> AdminUpdateReport200Response adminUpdateReport(id, adminUpdateReportRequest)

Update report status (Admin only)

Update resolution status of a reported item.

### Example

```ts
import {
  Configuration,
  ModerationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminUpdateReportOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ModerationApi(config);

  const body = {
    // string | Report ID
    id: id_example,
    // AdminUpdateReportRequest
    adminUpdateReportRequest: ...,
  } satisfies AdminUpdateReportOperationRequest;

  try {
    const data = await api.adminUpdateReport(body);
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
| **id** | `string` | Report ID | [Defaults to `undefined`] |
| **adminUpdateReportRequest** | [AdminUpdateReportRequest](AdminUpdateReportRequest.md) |  | |

### Return type

[**AdminUpdateReport200Response**](AdminUpdateReport200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Report status updated successfully |  -  |
| **400** | Bad request - invalid status |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |
| **404** | Report not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

