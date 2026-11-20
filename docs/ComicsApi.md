# ComicsApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getComicBySlug**](ComicsApi.md#getcomicbyslug) | **GET** /comics/{slug} | Get comic details by slug |
| [**getTrendingComics**](ComicsApi.md#gettrendingcomics) | **GET** /comics/trending | Get trending comics |
| [**listComics**](ComicsApi.md#listcomics) | **GET** /comics | List and filter comics |



## getComicBySlug

> GetComicBySlug200Response getComicBySlug(slug)

Get comic details by slug

Returns detailed metadata for a specific comic by slug, including genres, creators, and chapter list.

### Example

```ts
import {
  Configuration,
  ComicsApi,
} from '@komikhq/komikhq-typescript';
import type { GetComicBySlugRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new ComicsApi();

  const body = {
    // string | Unique comic slug identifier
    slug: slug_example,
  } satisfies GetComicBySlugRequest;

  try {
    const data = await api.getComicBySlug(body);
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
| **slug** | `string` | Unique comic slug identifier | [Defaults to `undefined`] |

### Return type

[**GetComicBySlug200Response**](GetComicBySlug200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comic details retrieved successfully. |  -  |
| **404** | Comic not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getTrendingComics

> GetTrendingComics200Response getTrendingComics(limit)

Get trending comics

Returns a list of trending and popular comics ranked by views.

### Example

```ts
import {
  Configuration,
  ComicsApi,
} from '@komikhq/komikhq-typescript';
import type { GetTrendingComicsRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new ComicsApi();

  const body = {
    // number | Max comics to return (max 50) (optional)
    limit: 56,
  } satisfies GetTrendingComicsRequest;

  try {
    const data = await api.getTrendingComics(body);
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
| **limit** | `number` | Max comics to return (max 50) | [Optional] [Defaults to `10`] |

### Return type

[**GetTrendingComics200Response**](GetTrendingComics200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Trending comics list. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listComics

> ListComics200Response listComics(q, genre, status, type, sort, page, limit)

List and filter comics

Returns a paginated list of comics with optional filters for genre, type, status, and sort.

### Example

```ts
import {
  Configuration,
  ComicsApi,
} from '@komikhq/komikhq-typescript';
import type { ListComicsRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new ComicsApi();

  const body = {
    // string | Search query string (optional)
    q: q_example,
    // string | Filter by genre slug (optional)
    genre: genre_example,
    // 'ongoing' | 'completed' | 'hiatus' (optional)
    status: status_example,
    // 'manga' | 'manhwa' | 'manhua' (optional)
    type: type_example,
    // 'latest' | 'popular' | 'updated' (optional)
    sort: sort_example,
    // number (optional)
    page: 56,
    // number (optional)
    limit: 56,
  } satisfies ListComicsRequest;

  try {
    const data = await api.listComics(body);
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
| **genre** | `string` | Filter by genre slug | [Optional] [Defaults to `undefined`] |
| **status** | `ongoing`, `completed`, `hiatus` |  | [Optional] [Defaults to `undefined`] [Enum: ongoing, completed, hiatus] |
| **type** | `manga`, `manhwa`, `manhua` |  | [Optional] [Defaults to `undefined`] [Enum: manga, manhwa, manhua] |
| **sort** | `latest`, `popular`, `updated` |  | [Optional] [Defaults to `undefined`] [Enum: latest, popular, updated] |
| **page** | `number` |  | [Optional] [Defaults to `1`] |
| **limit** | `number` |  | [Optional] [Defaults to `20`] |

### Return type

[**ListComics200Response**](ListComics200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated comic list. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

