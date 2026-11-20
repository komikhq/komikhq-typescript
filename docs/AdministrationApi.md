# AdministrationApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**adminCreateApiToken**](AdministrationApi.md#admincreateapitokenoperation) | **POST** /admin/api-tokens | Create a new API token |
| [**adminCreateChapter**](AdministrationApi.md#admincreatechapteroperation) | **POST** /admin/chapters | Create comic chapter |
| [**adminCreateChapterPages**](AdministrationApi.md#admincreatechapterpagesoperation) | **POST** /admin/chapters/{id}/pages | Set chapter pages |
| [**adminCreateComic**](AdministrationApi.md#admincreatecomic) | **POST** /admin/comics | Create a new comic |
| [**adminCreateGenre**](AdministrationApi.md#admincreategenreoperation) | **POST** /admin/genres | Create a new genre |
| [**adminCreateUser**](AdministrationApi.md#admincreateuseroperation) | **POST** /admin/users | Create new user account (Admin only) |
| [**adminDeleteChapter**](AdministrationApi.md#admindeletechapter) | **DELETE** /admin/chapters/{id} | Delete chapter by ID |
| [**adminDeleteComic**](AdministrationApi.md#admindeletecomic) | **DELETE** /admin/comics/{id} | Delete comic by ID |
| [**adminDeleteGenre**](AdministrationApi.md#admindeletegenre) | **DELETE** /admin/genres/{id} | Delete genre (Admin only) |
| [**adminDeleteUser**](AdministrationApi.md#admindeleteuser) | **DELETE** /admin/users/{id} | Delete user account (Admin only) |
| [**adminFinalizeChapter**](AdministrationApi.md#adminfinalizechapteroperation) | **POST** /admin/chapters/{id}/finalize | Finalize a chapter |
| [**adminGetChapter**](AdministrationApi.md#admingetchapter) | **GET** /admin/chapters/{id} | Get chapter details with pages |
| [**adminGetComic**](AdministrationApi.md#admingetcomic) | **GET** /admin/comics/{id} | Get comic details (Admin) |
| [**adminGetStats**](AdministrationApi.md#admingetstats) | **GET** /admin/stats | System overview stats (Admin only) |
| [**adminInitializeChapter**](AdministrationApi.md#admininitializechapteroperation) | **POST** /admin/chapters/init | Initialize a new chapter |
| [**adminListApiTokens**](AdministrationApi.md#adminlistapitokens) | **GET** /admin/api-tokens | List API tokens |
| [**adminListChapters**](AdministrationApi.md#adminlistchapters) | **GET** /admin/comics/{comicId}/chapters | List chapters for a comic |
| [**adminListComics**](AdministrationApi.md#adminlistcomics) | **GET** /admin/comics | List comics (Admin) |
| [**adminListGenres**](AdministrationApi.md#adminlistgenres) | **GET** /admin/genres | List all genres (Admin) |
| [**adminListUsers**](AdministrationApi.md#adminlistusers) | **GET** /admin/users | List registered users (Admin only) |
| [**adminRevokeApiToken**](AdministrationApi.md#adminrevokeapitoken) | **DELETE** /admin/api-tokens/{id} | Revoke an API token |
| [**adminUpdateChapter**](AdministrationApi.md#adminupdatechapteroperation) | **PUT** /admin/chapters/{id} | Update a chapter |
| [**adminUpdateComic**](AdministrationApi.md#adminupdatecomic) | **PUT** /admin/comics/{id} | Update comic by ID |
| [**adminUpdateGenre**](AdministrationApi.md#adminupdategenreoperation) | **PUT** /admin/genres/{id} | Update genre by ID |
| [**adminUpdateUser**](AdministrationApi.md#adminupdateuseroperation) | **PUT** /admin/users/{id} | Update user account (Admin only) |
| [**adminUploadChapterPage**](AdministrationApi.md#adminuploadchapterpage) | **POST** /admin/chapters/{id}/pages/upload | Upload chapter page image |



## adminCreateApiToken

> AdminCreateApiToken201Response adminCreateApiToken(adminCreateApiTokenRequest)

Create a new API token

Generates a new API token with specified scopes. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminCreateApiTokenOperationRequest } from '@komikhq/komikhq-typescript';

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
    // AdminCreateApiTokenRequest
    adminCreateApiTokenRequest: ...,
  } satisfies AdminCreateApiTokenOperationRequest;

  try {
    const data = await api.adminCreateApiToken(body);
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
| **adminCreateApiTokenRequest** | [AdminCreateApiTokenRequest](AdminCreateApiTokenRequest.md) |  | |

### Return type

[**AdminCreateApiToken201Response**](AdminCreateApiToken201Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | API token created. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminCreateChapter

> AdminFinalizeChapter200Response adminCreateChapter(adminCreateChapterRequest)

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

[**AdminFinalizeChapter200Response**](AdminFinalizeChapter200Response.md)

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

> AdminUpdateComic200Response adminCreateComic(title, slug, synopsis, creator, cover, coverUrlSource, coverUrl, banner, bannerUrlSource, bannerUrl, type, status, accessTier, genreIds)

Create a new comic

Inserts a new comic record into the catalog with support for direct file uploads or URLs. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminCreateComicRequest } from '@komikhq/komikhq-typescript';

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
    // string
    title: title_example,
    // string (optional)
    slug: slug_example,
    // string (optional)
    synopsis: synopsis_example,
    // string | Author / creator name (optional)
    creator: creator_example,
    // Blob | Cover image file (optional)
    cover: BINARY_DATA_HERE,
    // string | External cover image URL to download (optional)
    coverUrlSource: coverUrlSource_example,
    // string | Pre-existing storage object key (optional)
    coverUrl: coverUrl_example,
    // Blob | Banner image file (optional)
    banner: BINARY_DATA_HERE,
    // string | External banner image URL to download (optional)
    bannerUrlSource: bannerUrlSource_example,
    // string | Pre-existing storage object key (optional)
    bannerUrl: bannerUrl_example,
    // string (optional)
    type: type_example,
    // string (optional)
    status: status_example,
    // string (optional)
    accessTier: accessTier_example,
    // string | JSON stringified array of genre IDs (optional)
    genreIds: genreIds_example,
  } satisfies AdminCreateComicRequest;

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
| **title** | `string` |  | [Defaults to `undefined`] |
| **slug** | `string` |  | [Optional] [Defaults to `undefined`] |
| **synopsis** | `string` |  | [Optional] [Defaults to `undefined`] |
| **creator** | `string` | Author / creator name | [Optional] [Defaults to `undefined`] |
| **cover** | `Blob` | Cover image file | [Optional] [Defaults to `undefined`] |
| **coverUrlSource** | `string` | External cover image URL to download | [Optional] [Defaults to `undefined`] |
| **coverUrl** | `string` | Pre-existing storage object key | [Optional] [Defaults to `undefined`] |
| **banner** | `Blob` | Banner image file | [Optional] [Defaults to `undefined`] |
| **bannerUrlSource** | `string` | External banner image URL to download | [Optional] [Defaults to `undefined`] |
| **bannerUrl** | `string` | Pre-existing storage object key | [Optional] [Defaults to `undefined`] |
| **type** | `manga`, `manhwa`, `manhua` |  | [Optional] [Defaults to `&#39;manhwa&#39;`] [Enum: manga, manhwa, manhua] |
| **status** | `ongoing`, `completed`, `hiatus` |  | [Optional] [Defaults to `&#39;ongoing&#39;`] [Enum: ongoing, completed, hiatus] |
| **accessTier** | `string` |  | [Optional] [Defaults to `&#39;free&#39;`] |
| **genreIds** | `string` | JSON stringified array of genre IDs | [Optional] [Defaults to `undefined`] |

### Return type

[**AdminUpdateComic200Response**](AdminUpdateComic200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
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

Permanently deletes a comic record, cascade deletes chapters/pages, and purges storage assets. Requires administrator privileges.

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


## adminFinalizeChapter

> AdminFinalizeChapter200Response adminFinalizeChapter(id, adminFinalizeChapterRequest)

Finalize a chapter

Updates the chapter total pages count and refreshes the parent comic total chapters. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminFinalizeChapterOperationRequest } from '@komikhq/komikhq-typescript';

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
    // AdminFinalizeChapterRequest
    adminFinalizeChapterRequest: ...,
  } satisfies AdminFinalizeChapterOperationRequest;

  try {
    const data = await api.adminFinalizeChapter(body);
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
| **adminFinalizeChapterRequest** | [AdminFinalizeChapterRequest](AdminFinalizeChapterRequest.md) |  | |

### Return type

[**AdminFinalizeChapter200Response**](AdminFinalizeChapter200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chapter finalized successfully. |  -  |
| **400** | Invalid input. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |
| **404** | Chapter not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminGetChapter

> adminGetChapter(id)

Get chapter details with pages

Returns chapter metadata and ordered pages. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminGetChapterRequest } from '@komikhq/komikhq-typescript';

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
  } satisfies AdminGetChapterRequest;

  try {
    const data = await api.adminGetChapter(body);
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

`void` (Empty response body)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chapter details retrieved successfully. |  -  |
| **404** | Chapter not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminGetComic

> AdminGetComic200Response adminGetComic(id)

Get comic details (Admin)

Gets comic details by ID or slug with full genres, creators, and chapter list. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminGetComicRequest } from '@komikhq/komikhq-typescript';

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
  } satisfies AdminGetComicRequest;

  try {
    const data = await api.adminGetComic(body);
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

[**AdminGetComic200Response**](AdminGetComic200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The comic and its details. |  -  |
| **404** | Comic not found. |  -  |

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


## adminInitializeChapter

> AdminFinalizeChapter200Response adminInitializeChapter(adminInitializeChapterRequest)

Initialize a new chapter

Creates a new chapter with an auto-generated slug. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminInitializeChapterOperationRequest } from '@komikhq/komikhq-typescript';

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
    // AdminInitializeChapterRequest
    adminInitializeChapterRequest: ...,
  } satisfies AdminInitializeChapterOperationRequest;

  try {
    const data = await api.adminInitializeChapter(body);
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
| **adminInitializeChapterRequest** | [AdminInitializeChapterRequest](AdminInitializeChapterRequest.md) |  | |

### Return type

[**AdminFinalizeChapter200Response**](AdminFinalizeChapter200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chapter initialized successfully. |  -  |
| **400** | Invalid input. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminListApiTokens

> AdminListApiTokens200Response adminListApiTokens()

List API tokens

Lists active and revoked API tokens. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminListApiTokensRequest } from '@komikhq/komikhq-typescript';

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
    const data = await api.adminListApiTokens();
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

[**AdminListApiTokens200Response**](AdminListApiTokens200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of API tokens. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminListChapters

> AdminListChapters200Response adminListChapters(comicId)

List chapters for a comic

Returns all chapters for a given comic, ordered by chapter number. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminListChaptersRequest } from '@komikhq/komikhq-typescript';

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
    comicId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies AdminListChaptersRequest;

  try {
    const data = await api.adminListChapters(body);
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

[**AdminListChapters200Response**](AdminListChapters200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chapters listed successfully. |  -  |
| **400** | Invalid input. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminListComics

> AdminListComics200Response adminListComics(q, status, page, limit)

List comics (Admin)

Lists comics with search, status filtering, and pagination. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminListComicsRequest } from '@komikhq/komikhq-typescript';

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
    // string | Search query string (optional)
    q: q_example,
    // string | Filter by status (optional)
    status: status_example,
    // number (optional)
    page: 56,
    // number (optional)
    limit: 56,
  } satisfies AdminListComicsRequest;

  try {
    const data = await api.adminListComics(body);
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
| **q** | `string` | Search query string | [Optional] [Defaults to `undefined`] |
| **status** | `string` | Filter by status | [Optional] [Defaults to `undefined`] |
| **page** | `number` |  | [Optional] [Defaults to `1`] |
| **limit** | `number` |  | [Optional] [Defaults to `15`] |

### Return type

[**AdminListComics200Response**](AdminListComics200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Matching comics and pagination metadata. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminListGenres

> AdminListGenres200Response adminListGenres()

List all genres (Admin)

Returns all genres. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminListGenresRequest } from '@komikhq/komikhq-typescript';

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
    const data = await api.adminListGenres();
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

[**AdminListGenres200Response**](AdminListGenres200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The genre catalog. |  -  |

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


## adminRevokeApiToken

> AdminRevokeApiToken200Response adminRevokeApiToken(id)

Revoke an API token

Revokes and deletes an API token by ID. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminRevokeApiTokenRequest } from '@komikhq/komikhq-typescript';

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
    // string | Token ID
    id: id_example,
  } satisfies AdminRevokeApiTokenRequest;

  try {
    const data = await api.adminRevokeApiToken(body);
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
| **id** | `string` | Token ID | [Defaults to `undefined`] |

### Return type

[**AdminRevokeApiToken200Response**](AdminRevokeApiToken200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Token revoked successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminUpdateChapter

> AdminFinalizeChapter200Response adminUpdateChapter(id, adminUpdateChapterRequest)

Update a chapter

Updates chapter details. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminUpdateChapterOperationRequest } from '@komikhq/komikhq-typescript';

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
    // AdminUpdateChapterRequest
    adminUpdateChapterRequest: ...,
  } satisfies AdminUpdateChapterOperationRequest;

  try {
    const data = await api.adminUpdateChapter(body);
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
| **adminUpdateChapterRequest** | [AdminUpdateChapterRequest](AdminUpdateChapterRequest.md) |  | |

### Return type

[**AdminFinalizeChapter200Response**](AdminFinalizeChapter200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chapter updated successfully. |  -  |
| **400** | Invalid input. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |
| **404** | Chapter not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminUpdateComic

> AdminUpdateComic200Response adminUpdateComic(id, title, slug, synopsis, creator, cover, coverUrlSource, coverUrl, banner, bannerUrlSource, bannerUrl, type, status, accessTier, genreIds)

Update comic by ID

Updates comic metadata by ID with support for direct file uploads or JSON. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminUpdateComicRequest } from '@komikhq/komikhq-typescript';

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
    // string (optional)
    title: title_example,
    // string (optional)
    slug: slug_example,
    // string (optional)
    synopsis: synopsis_example,
    // string (optional)
    creator: creator_example,
    // Blob | Cover image file (optional)
    cover: BINARY_DATA_HERE,
    // string | External cover image URL to download (optional)
    coverUrlSource: coverUrlSource_example,
    // string | Pre-existing storage object key (optional)
    coverUrl: coverUrl_example,
    // Blob | Banner image file (optional)
    banner: BINARY_DATA_HERE,
    // string | External banner image URL to download (optional)
    bannerUrlSource: bannerUrlSource_example,
    // string | Pre-existing storage object key (optional)
    bannerUrl: bannerUrl_example,
    // string (optional)
    type: type_example,
    // string (optional)
    status: status_example,
    // string (optional)
    accessTier: accessTier_example,
    // string | JSON stringified array of genre IDs (optional)
    genreIds: genreIds_example,
  } satisfies AdminUpdateComicRequest;

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
| **title** | `string` |  | [Optional] [Defaults to `undefined`] |
| **slug** | `string` |  | [Optional] [Defaults to `undefined`] |
| **synopsis** | `string` |  | [Optional] [Defaults to `undefined`] |
| **creator** | `string` |  | [Optional] [Defaults to `undefined`] |
| **cover** | `Blob` | Cover image file | [Optional] [Defaults to `undefined`] |
| **coverUrlSource** | `string` | External cover image URL to download | [Optional] [Defaults to `undefined`] |
| **coverUrl** | `string` | Pre-existing storage object key | [Optional] [Defaults to `undefined`] |
| **banner** | `Blob` | Banner image file | [Optional] [Defaults to `undefined`] |
| **bannerUrlSource** | `string` | External banner image URL to download | [Optional] [Defaults to `undefined`] |
| **bannerUrl** | `string` | Pre-existing storage object key | [Optional] [Defaults to `undefined`] |
| **type** | `manga`, `manhwa`, `manhua` |  | [Optional] [Defaults to `undefined`] [Enum: manga, manhwa, manhua] |
| **status** | `ongoing`, `completed`, `hiatus` |  | [Optional] [Defaults to `undefined`] [Enum: ongoing, completed, hiatus] |
| **accessTier** | `string` |  | [Optional] [Defaults to `undefined`] |
| **genreIds** | `string` | JSON stringified array of genre IDs | [Optional] [Defaults to `undefined`] |

### Return type

[**AdminUpdateComic200Response**](AdminUpdateComic200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
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


## adminUploadChapterPage

> AdminUploadChapterPage200Response adminUploadChapterPage(id, file, pageNumber, width, height)

Upload chapter page image

Uploads a single page image file directly to R2 storage and associates it with the specified chapter. Requires administrator privileges.

### Example

```ts
import {
  Configuration,
  AdministrationApi,
} from '@komikhq/komikhq-typescript';
import type { AdminUploadChapterPageRequest } from '@komikhq/komikhq-typescript';

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
    // Blob | Image file
    file: BINARY_DATA_HERE,
    // number | Page order index
    pageNumber: 56,
    // number | Optional image width (optional)
    width: 56,
    // number | Optional image height (optional)
    height: 56,
  } satisfies AdminUploadChapterPageRequest;

  try {
    const data = await api.adminUploadChapterPage(body);
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
| **file** | `Blob` | Image file | [Defaults to `undefined`] |
| **pageNumber** | `number` | Page order index | [Defaults to `undefined`] |
| **width** | `number` | Optional image width | [Optional] [Defaults to `undefined`] |
| **height** | `number` | Optional image height | [Optional] [Defaults to `undefined`] |

### Return type

[**AdminUploadChapterPage200Response**](AdminUploadChapterPage200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chapter page uploaded successfully. |  -  |
| **400** | Invalid input or file missing. |  -  |
| **401** | Unauthorized. |  -  |
| **403** | Forbidden. |  -  |
| **404** | Chapter not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

