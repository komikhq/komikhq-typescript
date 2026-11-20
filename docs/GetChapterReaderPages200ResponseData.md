
# GetChapterReaderPages200ResponseData


## Properties

Name | Type
------------ | -------------
`comic` | [GetChapterReaderPages200ResponseDataComic](GetChapterReaderPages200ResponseDataComic.md)
`chapter` | [Chapter](Chapter.md)
`pages` | [Array&lt;ChapterPage&gt;](ChapterPage.md)
`allChapters` | [Array&lt;GetChapterReaderPages200ResponseDataAllChaptersInner&gt;](GetChapterReaderPages200ResponseDataAllChaptersInner.md)
`prevChapter` | [GetChapterReaderPages200ResponseDataPrevChapter](GetChapterReaderPages200ResponseDataPrevChapter.md)
`nextChapter` | [GetChapterReaderPages200ResponseDataPrevChapter](GetChapterReaderPages200ResponseDataPrevChapter.md)

## Example

```typescript
import type { GetChapterReaderPages200ResponseData } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "comic": null,
  "chapter": null,
  "pages": null,
  "allChapters": null,
  "prevChapter": null,
  "nextChapter": null,
} satisfies GetChapterReaderPages200ResponseData

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as GetChapterReaderPages200ResponseData
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


