# SitemapsApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getChaptersSitemapXml**](SitemapsApi.md#getchapterssitemapxml) | **GET** /sitemaps/sitemap-chapters.xml | Chapters XML sitemap |
| [**getComicsSitemapXml**](SitemapsApi.md#getcomicssitemapxml) | **GET** /sitemaps/sitemap-comics.xml | Comics XML sitemap |
| [**getSitemapSummary**](SitemapsApi.md#getsitemapsummary) | **GET** /sitemaps/summary | Sitemap summary statistics |
| [**listSitemapChapters**](SitemapsApi.md#listsitemapchapters) | **GET** /sitemaps/chapters | List chapters for sitemap |
| [**listSitemapComics**](SitemapsApi.md#listsitemapcomics) | **GET** /sitemaps/comics | List comics for sitemap |



## getChaptersSitemapXml

> getChaptersSitemapXml(format)

Chapters XML sitemap

Generates XML sitemap of all published comic chapters for search engine bots. Supports JSON output via ?format&#x3D;json or Accept: application/json.

### Example

```ts
import {
  Configuration,
  SitemapsApi,
} from '@komikhq/komikhq-typescript';
import type { GetChaptersSitemapXmlRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new SitemapsApi();

  const body = {
    // 'xml' | 'json' | Output format (xml or json) (optional)
    format: format_example,
  } satisfies GetChaptersSitemapXmlRequest;

  try {
    const data = await api.getChaptersSitemapXml(body);
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
| **format** | `xml`, `json` | Output format (xml or json) | [Optional] [Defaults to `&#39;xml&#39;`] [Enum: xml, json] |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/xml`, `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | XML sitemap or JSON feed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getComicsSitemapXml

> getComicsSitemapXml(format)

Comics XML sitemap

Generates XML sitemap of all published comics for search engine bots. Supports JSON output via ?format&#x3D;json or Accept: application/json.

### Example

```ts
import {
  Configuration,
  SitemapsApi,
} from '@komikhq/komikhq-typescript';
import type { GetComicsSitemapXmlRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new SitemapsApi();

  const body = {
    // 'xml' | 'json' | Output format (xml or json) (optional)
    format: format_example,
  } satisfies GetComicsSitemapXmlRequest;

  try {
    const data = await api.getComicsSitemapXml(body);
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
| **format** | `xml`, `json` | Output format (xml or json) | [Optional] [Defaults to `&#39;xml&#39;`] [Enum: xml, json] |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/xml`, `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | XML sitemap or JSON feed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getSitemapSummary

> GetSitemapSummary200Response getSitemapSummary()

Sitemap summary statistics

Returns the latest update timestamps and total counts for comics and chapters, useful for sitemap index generation.

### Example

```ts
import {
  Configuration,
  SitemapsApi,
} from '@komikhq/komikhq-typescript';
import type { GetSitemapSummaryRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new SitemapsApi();

  try {
    const data = await api.getSitemapSummary();
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

[**GetSitemapSummary200Response**](GetSitemapSummary200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sitemap summary with latest updates and totals. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listSitemapChapters

> ListSitemapChapters200Response listSitemapChapters(page, limit)

List chapters for sitemap

Returns a paginated list of chapters with their comic slug for sitemap generation.

### Example

```ts
import {
  Configuration,
  SitemapsApi,
} from '@komikhq/komikhq-typescript';
import type { ListSitemapChaptersRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new SitemapsApi();

  const body = {
    // number | Page number. (optional)
    page: 56,
    // number | Number of chapters per page. (optional)
    limit: 56,
  } satisfies ListSitemapChaptersRequest;

  try {
    const data = await api.listSitemapChapters(body);
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
| **page** | `number` | Page number. | [Optional] [Defaults to `1`] |
| **limit** | `number` | Number of chapters per page. | [Optional] [Defaults to `1000`] |

### Return type

[**ListSitemapChapters200Response**](ListSitemapChapters200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Paginated list of chapters for sitemap. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listSitemapComics

> ListSitemapComics200Response listSitemapComics(limit)

List comics for sitemap

Returns a list of comic slugs and their last update timestamps for sitemap generation.

### Example

```ts
import {
  Configuration,
  SitemapsApi,
} from '@komikhq/komikhq-typescript';
import type { ListSitemapComicsRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new SitemapsApi();

  const body = {
    // number | Maximum number of comics to return. (optional)
    limit: 56,
  } satisfies ListSitemapComicsRequest;

  try {
    const data = await api.listSitemapComics(body);
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
| **limit** | `number` | Maximum number of comics to return. | [Optional] [Defaults to `50000`] |

### Return type

[**ListSitemapComics200Response**](ListSitemapComics200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of comics with slug and updatedAt. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

