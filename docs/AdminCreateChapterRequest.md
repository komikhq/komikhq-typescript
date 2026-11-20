
# AdminCreateChapterRequest


## Properties

Name | Type
------------ | -------------
`comicId` | string
`chapterNumber` | string
`title` | string
`slug` | string
`accessTier` | string
`isEarlyAccess` | boolean

## Example

```typescript
import type { AdminCreateChapterRequest } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "comicId": null,
  "chapterNumber": null,
  "title": null,
  "slug": null,
  "accessTier": null,
  "isEarlyAccess": null,
} satisfies AdminCreateChapterRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AdminCreateChapterRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


