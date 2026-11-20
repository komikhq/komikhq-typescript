# SitemapsApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getComicSitemapXml**](SitemapsApi.md#getcomicsitemapxml) | **GET** /sitemap | XML sitemap generator |



## getComicSitemapXml

> getComicSitemapXml()

XML sitemap generator

Generates dynamic XML sitemap of all indexed comics for search engine bots.

### Example

```ts
import {
  Configuration,
  SitemapsApi,
} from '@komikhq/komikhq-typescript';
import type { GetComicSitemapXmlRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new SitemapsApi();

  try {
    const data = await api.getComicSitemapXml();
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

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/xml`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | XML sitemap content. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

