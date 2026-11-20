# BookmarksApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteBookmark**](BookmarksApi.md#deletebookmark) | **DELETE** /bookmarks/{comicId} | Remove comic bookmark |
| [**listBookmarks**](BookmarksApi.md#listbookmarks) | **GET** /bookmarks | List user bookmarks |
| [**upsertBookmark**](BookmarksApi.md#upsertbookmarkoperation) | **POST** /bookmarks | Add or update comic bookmark |



## deleteBookmark

> SuccessResponse deleteBookmark(comicId)

Remove comic bookmark

Deletes a comic from the user\&#39;s bookmarks list.

### Example

```ts
import {
  Configuration,
  BookmarksApi,
} from '@komikhq/komikhq-typescript';
import type { DeleteBookmarkRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BookmarksApi(config);

  const body = {
    // string | Comic ID
    comicId: comicId_example,
  } satisfies DeleteBookmarkRequest;

  try {
    const data = await api.deleteBookmark(body);
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
| **200** | Bookmark removed successfully. |  -  |
| **401** | Unauthorized. |  -  |
| **404** | Bookmark not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listBookmarks

> ListBookmarks200Response listBookmarks()

List user bookmarks

Returns all saved comic bookmarks for the authenticated user.

### Example

```ts
import {
  Configuration,
  BookmarksApi,
} from '@komikhq/komikhq-typescript';
import type { ListBookmarksRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BookmarksApi(config);

  try {
    const data = await api.listBookmarks();
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

[**ListBookmarks200Response**](ListBookmarks200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User bookmarks list. |  -  |
| **401** | Unauthorized. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## upsertBookmark

> UpsertBookmark200Response upsertBookmark(upsertBookmarkRequest)

Add or update comic bookmark

Saves a comic to user bookmarks with a reading status (reading, completed, plan_to_read, dropped).

### Example

```ts
import {
  Configuration,
  BookmarksApi,
} from '@komikhq/komikhq-typescript';
import type { UpsertBookmarkOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BookmarksApi(config);

  const body = {
    // UpsertBookmarkRequest
    upsertBookmarkRequest: ...,
  } satisfies UpsertBookmarkOperationRequest;

  try {
    const data = await api.upsertBookmark(body);
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
| **upsertBookmarkRequest** | [UpsertBookmarkRequest](UpsertBookmarkRequest.md) |  | |

### Return type

[**UpsertBookmark200Response**](UpsertBookmark200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bookmark saved successfully. |  -  |
| **400** | Invalid payload. |  -  |
| **401** | Unauthorized. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

