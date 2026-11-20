# AdministrationApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**adminCreateChapter**](AdministrationApi.md#admincreatechapteroperation) | **POST** /admin/chapters | Create comic chapter |
| [**adminCreateChapterPages**](AdministrationApi.md#admincreatechapterpagesoperation) | **POST** /admin/chapters/{id}/pages | Set chapter pages |
| [**adminCreateComic**](AdministrationApi.md#admincreatecomicoperation) | **POST** /admin/comics | Create a new comic |
| [**adminCreateGenre**](AdministrationApi.md#admincreategenreoperation) | **POST** /admin/genres | Create a new genre |
| [**adminCreateUser**](AdministrationApi.md#admincreateuseroperation) | **POST** /admin/users | Create new user account (Admin only) |
| [**adminDeleteChapter**](AdministrationApi.md#admindeletechapter) | **DELETE** /admin/chapters/{id} | Delete chapter by ID |
| [**adminDeleteComic**](AdministrationApi.md#admindeletecomic) | **DELETE** /admin/comics/{id} | Delete comic by ID |
| [**adminDeleteGenre**](AdministrationApi.md#admindeletegenre) | **DELETE** /admin/genres/{id} | Delete genre (Admin only) |
| [**adminDeleteUser**](AdministrationApi.md#admindeleteuser) | **DELETE** /admin/users/{id} | Delete user account (Admin only) |
| [**adminGetStats**](AdministrationApi.md#admingetstats) | **GET** /admin/stats | System overview stats (Admin only) |
| [**adminListUsers**](AdministrationApi.md#adminlistusers) | **GET** /admin/users | List registered users (Admin only) |
| [**adminUpdateComic**](AdministrationApi.md#adminupdatecomicoperation) | **PUT** /admin/comics/{id} | Update comic by ID |
| [**adminUpdateGenre**](AdministrationApi.md#adminupdategenreoperation) | **PUT** /admin/genres/{id} | Update genre by ID |
| [**adminUpdateUser**](AdministrationApi.md#adminupdateuseroperation) | **PUT** /admin/users/{id} | Update user account (Admin only) |



## adminCreateChapter

> AdminCreateChapter200Response adminCreateChapter(adminCreateChapterRequest)

Create comic chapter

Inserts a new comic chapter into the database. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminCreateChapterOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // AdminCreateChapterRequest
    adminCreateChapterRequest: ...,
  } satisfies AdminCreateChapterOperationRequest;

  try {
    const data = await api.adminCreateChapter(body);
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
| **adminCreateChapterRequest** | [AdminCreateChapterRequest](AdminCreateChapterRequest.md) |  | |

### Return type

[**AdminCreateChapter200Response**](AdminCreateChapter200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chapter created successfully. |  -  |
| **400** | Invalid input. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminCreateChapterPages

> AdminCreateChapterPages200Response adminCreateChapterPages(id, adminCreateChapterPagesRequest)

Set chapter pages

Replaces and reorders all pages for a chapter. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminCreateChapterPagesOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // string | Chapter ID
    id: id_example,
    // AdminCreateChapterPagesRequest
    adminCreateChapterPagesRequest: ...,
  } satisfies AdminCreateChapterPagesOperationRequest;

  try {
    const data = await api.adminCreateChapterPages(body);
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
| **id** | `string` | Chapter ID | [Defaults to `undefined`] |
| **adminCreateChapterPagesRequest** | [AdminCreateChapterPagesRequest](AdminCreateChapterPagesRequest.md) |  | |

### Return type

[**AdminCreateChapterPages200Response**](AdminCreateChapterPages200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chapter pages updated successfully. |  -  |
| **400** | Invalid pages array. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminCreateComic

> AdminUpdateComic200Response adminCreateComic(adminCreateComicRequest)

Create a new comic

Inserts a new comic record into the catalog. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminCreateComicOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // AdminCreateComicRequest
    adminCreateComicRequest: ...,
  } satisfies AdminCreateComicOperationRequest;

  try {
    const data = await api.adminCreateComic(body);
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
| **adminCreateComicRequest** | [AdminCreateComicRequest](AdminCreateComicRequest.md) |  | |

### Return type

[**AdminUpdateComic200Response**](AdminUpdateComic200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comic created successfully. |  -  |
| **400** | Invalid input. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminCreateGenre

> AdminUpdateGenre200Response adminCreateGenre(adminCreateGenreRequest)

Create a new genre

Inserts a new comic genre into the database. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminCreateGenreOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // AdminCreateGenreRequest
    adminCreateGenreRequest: ...,
  } satisfies AdminCreateGenreOperationRequest;

  try {
    const data = await api.adminCreateGenre(body);
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
| **adminCreateGenreRequest** | [AdminCreateGenreRequest](AdminCreateGenreRequest.md) |  | |

### Return type

[**AdminUpdateGenre200Response**](AdminUpdateGenre200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Genre created successfully. |  -  |
| **400** | Invalid input. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminCreateUser

> AdminUpdateUser200Response adminCreateUser(adminCreateUserRequest)

Create new user account (Admin only)

Provision a new user account with custom credentials and role.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminCreateUserOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // AdminCreateUserRequest
    adminCreateUserRequest: ...,
  } satisfies AdminCreateUserOperationRequest;

  try {
    const data = await api.adminCreateUser(body);
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
| **adminCreateUserRequest** | [AdminCreateUserRequest](AdminCreateUserRequest.md) |  | |

### Return type

[**AdminUpdateUser200Response**](AdminUpdateUser200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User created successfully |  -  |
| **400** | Invalid input or user already exists |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminDeleteChapter

> SuccessResponse adminDeleteChapter(id)

Delete chapter by ID

Permanently deletes a chapter record and its pages from the database. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminDeleteChapterRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // string | Chapter ID
    id: id_example,
  } satisfies AdminDeleteChapterRequest;

  try {
    const data = await api.adminDeleteChapter(body);
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
| **id** | `string` | Chapter ID | [Defaults to `undefined`] |

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
| **200** | Chapter deleted successfully. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |
| **404** | Chapter not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminDeleteComic

> SuccessResponse adminDeleteComic(id)

Delete comic by ID

Permanently deletes a comic record and all its associated chapters. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminDeleteComicRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // string | Comic ID
    id: id_example,
  } satisfies AdminDeleteComicRequest;

  try {
    const data = await api.adminDeleteComic(body);
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
| **id** | `string` | Comic ID | [Defaults to `undefined`] |

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
| **200** | Comic deleted successfully. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |
| **404** | Comic not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminDeleteGenre

> SuccessResponse adminDeleteGenre(id)

Delete genre (Admin only)

Permanently delete an existing comic genre.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminDeleteGenreRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // string | Genre ID to delete
    id: id_example,
  } satisfies AdminDeleteGenreRequest;

  try {
    const data = await api.adminDeleteGenre(body);
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
| **id** | `string` | Genre ID to delete | [Defaults to `undefined`] |

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
| **200** | Genre deleted successfully |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |
| **404** | Genre not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminDeleteUser

> SuccessResponse adminDeleteUser(id)

Delete user account (Admin only)

Permanently delete a user account and their storage assets.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminDeleteUserRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // string | User ID
    id: id_example,
  } satisfies AdminDeleteUserRequest;

  try {
    const data = await api.adminDeleteUser(body);
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
| **id** | `string` | User ID | [Defaults to `undefined`] |

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
| **200** | User deleted successfully |  -  |
| **400** | Bad request - cannot delete own account |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |
| **404** | User not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminGetStats

> AdminGetStats200Response adminGetStats()

System overview stats (Admin only)

Get aggregate metrics for comics, chapters, users, and comments.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminGetStatsRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  try {
    const data = await api.adminGetStats();
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

[**AdminGetStats200Response**](AdminGetStats200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dashboard stats summary |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminListUsers

> AdminListUsers200Response adminListUsers(q, page, limit)

List registered users (Admin only)

Paginated user list with optional search query.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminListUsersRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // string | Search keyword for name or email (optional)
    q: q_example,
    // number | Page number (optional)
    page: 56,
    // number | Items per page (optional)
    limit: 56,
  } satisfies AdminListUsersRequest;

  try {
    const data = await api.adminListUsers(body);
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
| **q** | `string` | Search keyword for name or email | [Optional] [Defaults to `undefined`] |
| **page** | `number` | Page number | [Optional] [Defaults to `1`] |
| **limit** | `number` | Items per page | [Optional] [Defaults to `20`] |

### Return type

[**AdminListUsers200Response**](AdminListUsers200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated list of users |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminUpdateComic

> AdminUpdateComic200Response adminUpdateComic(id, adminUpdateComicRequest)

Update comic by ID

Updates comic metadata by ID. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminUpdateComicOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // string | Comic ID
    id: id_example,
    // AdminUpdateComicRequest (optional)
    adminUpdateComicRequest: ...,
  } satisfies AdminUpdateComicOperationRequest;

  try {
    const data = await api.adminUpdateComic(body);
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
| **id** | `string` | Comic ID | [Defaults to `undefined`] |
| **adminUpdateComicRequest** | [AdminUpdateComicRequest](AdminUpdateComicRequest.md) |  | [Optional] |

### Return type

[**AdminUpdateComic200Response**](AdminUpdateComic200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comic updated successfully. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |
| **404** | Comic not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminUpdateGenre

> AdminUpdateGenre200Response adminUpdateGenre(id, adminUpdateGenreRequest)

Update genre by ID

Modifies genre name, slug, or description. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminUpdateGenreOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // string | Genre ID
    id: id_example,
    // AdminUpdateGenreRequest (optional)
    adminUpdateGenreRequest: ...,
  } satisfies AdminUpdateGenreOperationRequest;

  try {
    const data = await api.adminUpdateGenre(body);
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
| **id** | `string` | Genre ID | [Defaults to `undefined`] |
| **adminUpdateGenreRequest** | [AdminUpdateGenreRequest](AdminUpdateGenreRequest.md) |  | [Optional] |

### Return type

[**AdminUpdateGenre200Response**](AdminUpdateGenre200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Genre updated successfully. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |
| **404** | Genre not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminUpdateUser

> AdminUpdateUser200Response adminUpdateUser(id, adminUpdateUserRequest)

Update user account (Admin only)

Update details, role, or reset password for an existing user account.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminUpdateUserOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdministrationApi(config);

  const body = {
    // string | User ID
    id: id_example,
    // AdminUpdateUserRequest
    adminUpdateUserRequest: ...,
  } satisfies AdminUpdateUserOperationRequest;

  try {
    const data = await api.adminUpdateUser(body);
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
| **id** | `string` | User ID | [Defaults to `undefined`] |
| **adminUpdateUserRequest** | [AdminUpdateUserRequest](AdminUpdateUserRequest.md) |  | |

### Return type

[**AdminUpdateUser200Response**](AdminUpdateUser200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User account updated successfully |  -  |
| **400** | Invalid input |  -  |
| **401** | Unauthorized |  -  |
| **403** | Forbidden - Admin access required |  -  |
| **404** | User not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

