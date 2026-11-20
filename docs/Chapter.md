
# Chapter


## Properties

Name | Type
------------ | -------------
`id` | string
`comicId` | string
`chapterNumber` | string
`title` | string
`slug` | string
`totalPages` | number
`totalViews` | number
`publishedAt` | Date

## Example

```typescript
import type { Chapter } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "comicId": null,
  "chapterNumber": null,
  "title": null,
  "slug": null,
  "totalPages": null,
  "totalViews": null,
  "publishedAt": null,
} satisfies Chapter

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Chapter
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


