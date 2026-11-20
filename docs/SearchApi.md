# SearchApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getSearchSuggestions**](SearchApi.md#getsearchsuggestions) | **GET** /search/suggest | Instant search autocomplete suggestions |
| [**searchComics**](SearchApi.md#searchcomics) | **GET** /search | Full text comic search |



## getSearchSuggestions

> GetSearchSuggestions200Response getSearchSuggestions(q, limit)

Instant search autocomplete suggestions

Returns scored autocomplete search suggestions using CTE matching with KV caching.

### Example

```ts
import {
  Configuration,
  SearchApi,
} from '@komikhq/komikhq-typescript';
import type { GetSearchSuggestionsRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new SearchApi();

  const body = {
    // string | Partial query string
    q: q_example,
    // number | Max suggestions (optional)
    limit: 56,
  } satisfies GetSearchSuggestionsRequest;

  try {
    const data = await api.getSearchSuggestions(body);
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
| **q** | `string` | Partial query string | [Defaults to `undefined`] |
| **limit** | `number` | Max suggestions | [Optional] [Defaults to `8`] |

### Return type

[**GetSearchSuggestions200Response**](GetSearchSuggestions200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Search suggestions list. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## searchComics

> ListComics200Response searchComics(q, page, limit)

Full text comic search

Searches comics across titles, alternate titles, and slugs with pagination.

### Example

```ts
import {
  Configuration,
  SearchApi,
} from '@komikhq/komikhq-typescript';
import type { SearchComicsRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new SearchApi();

  const body = {
    // string | Search query (optional)
    q: q_example,
    // number (optional)
    page: 56,
    // number (optional)
    limit: 56,
  } satisfies SearchComicsRequest;

  try {
    const data = await api.searchComics(body);
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
| **q** | `string` | Search query | [Optional] [Defaults to `undefined`] |
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
| **200** | Search results list. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

