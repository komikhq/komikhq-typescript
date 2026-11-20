
# GetSitemapSummary200ResponseData


## Properties

Name | Type
------------ | -------------
`latestComicUpdate` | Date
`latestChapterUpdate` | Date
`totalComics` | number
`totalChapters` | number

## Example

```typescript
import type { GetSitemapSummary200ResponseData } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "latestComicUpdate": null,
  "latestChapterUpdate": null,
  "totalComics": null,
  "totalChapters": null,
} satisfies GetSitemapSummary200ResponseData

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as GetSitemapSummary200ResponseData
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


