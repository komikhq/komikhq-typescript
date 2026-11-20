# ChaptersApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getChapterReaderPages**](ChaptersApi.md#getchapterreaderpages) | **GET** /comics/{comicSlug}/chapters/{chapterSlug} | Get chapter reader pages and navigation |



## getChapterReaderPages

> GetChapterReaderPages200Response getChapterReaderPages(comicSlug, chapterSlug)

Get chapter reader pages and navigation

Returns chapter pages with CDN image URLs and previous/next chapter navigation.

### Example

```ts
import {
  Configuration,
  ChaptersApi,
} from '@komikhq/komikhq-typescript';
import type { GetChapterReaderPagesRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const api = new ChaptersApi();

  const body = {
    // string | Comic slug
    comicSlug: comicSlug_example,
    // string | Chapter slug
    chapterSlug: chapterSlug_example,
  } satisfies GetChapterReaderPagesRequest;

  try {
    const data = await api.getChapterReaderPages(body);
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
| **comicSlug** | `string` | Comic slug | [Defaults to `undefined`] |
| **chapterSlug** | `string` | Chapter slug | [Defaults to `undefined`] |

### Return type

[**GetChapterReaderPages200Response**](GetChapterReaderPages200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chapter reader pages retrieved successfully. |  -  |
| **404** | Chapter or comic not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

