# CommentsApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createComment**](CommentsApi.md#createcommentoperation) | **POST** /comments | Post a comment or reply |
| [**deleteComment**](CommentsApi.md#deletecomment) | **DELETE** /comments/{id} | Delete comment |
| [**listComments**](CommentsApi.md#listcomments) | **GET** /comments | List comments for comic or chapter |
| [**reportComment**](CommentsApi.md#reportcommentoperation) | **POST** /comments/{id}/report | Report an inappropriate comment |
| [**toggleCommentLike**](CommentsApi.md#togglecommentlike) | **POST** /comments/{id}/like | Toggle like on comment |



## createComment

> CreateComment200Response createComment(createCommentRequest)

Post a comment or reply

Posts a new comment or nested reply for a comic or specific chapter.

### Example

```ts
import {
  Configuration,
  CommentsApi,
} from '@komikhq/komikhq-typescript';
import type { CreateCommentOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new CommentsApi();

  const body = {
    // CreateCommentRequest
    createCommentRequest: ...,
  } satisfies CreateCommentOperationRequest;

  try {
    const data = await api.createComment(body);
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
| **createCommentRequest** | [CreateCommentRequest](CreateCommentRequest.md) |  | |

### Return type

[**CreateComment200Response**](CreateComment200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comment created successfully. |  -  |
| **400** | Invalid payload. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deleteComment

> SuccessResponse deleteComment(id)

Delete comment

Deletes a comment. Only the author or an administrator can perform this action.

### Example

```ts
import {
  Configuration,
  CommentsApi,
} from '@komikhq/komikhq-typescript';
import type { DeleteCommentRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CommentsApi(config);

  const body = {
    // string | Comment ID
    id: id_example,
  } satisfies DeleteCommentRequest;

  try {
    const data = await api.deleteComment(body);
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
| **id** | `string` | Comment ID | [Defaults to `undefined`] |

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
| **200** | Comment deleted successfully. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |
| **404** | Comment not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listComments

> ListComments200Response listComments(comicId, chapterId)

List comments for comic or chapter

Returns nested threaded comments with like states and author information.

### Example

```ts
import {
  Configuration,
  CommentsApi,
} from '@komikhq/komikhq-typescript';
import type { ListCommentsRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new CommentsApi();

  const body = {
    // string | Comic ID
    comicId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string | Optional chapter ID filter (optional)
    chapterId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListCommentsRequest;

  try {
    const data = await api.listComments(body);
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
| **chapterId** | `string` | Optional chapter ID filter | [Optional] [Defaults to `undefined`] |

### Return type

[**ListComments200Response**](ListComments200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comments thread list. |  -  |
| **400** | comicId is missing. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## reportComment

> SuccessResponse reportComment(id, reportCommentRequest)

Report an inappropriate comment

Submits a moderation report for a comment with a specific violation reason.

### Example

```ts
import {
  Configuration,
  CommentsApi,
} from '@komikhq/komikhq-typescript';
import type { ReportCommentOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new CommentsApi();

  const body = {
    // string | Comment ID
    id: id_example,
    // ReportCommentRequest
    reportCommentRequest: ...,
  } satisfies ReportCommentOperationRequest;

  try {
    const data = await api.reportComment(body);
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
| **id** | `string` | Comment ID | [Defaults to `undefined`] |
| **reportCommentRequest** | [ReportCommentRequest](ReportCommentRequest.md) |  | |

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Report submitted. |  -  |
| **400** | Invalid payload. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## toggleCommentLike

> ToggleCommentLike200Response toggleCommentLike(id)

Toggle like on comment

Adds or removes a like on the specified comment for the authenticated user.

### Example

```ts
import {
  Configuration,
  CommentsApi,
} from '@komikhq/komikhq-typescript';
import type { ToggleCommentLikeRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CommentsApi(config);

  const body = {
    // string | Comment ID
    id: id_example,
  } satisfies ToggleCommentLikeRequest;

  try {
    const data = await api.toggleCommentLike(body);
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
| **id** | `string` | Comment ID | [Defaults to `undefined`] |

### Return type

[**ToggleCommentLike200Response**](ToggleCommentLike200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Like status toggled. |  -  |
| **401** | Unauthorized. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

