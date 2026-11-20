
# AdminUpdateChapterRequest


## Properties

Name | Type
------------ | -------------
`chapterNumber` | string
`title` | string
`accessTier` | string
`isEarlyAccess` | boolean

## Example

```typescript
import type { AdminUpdateChapterRequest } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "chapterNumber": null,
  "title": null,
  "accessTier": null,
  "isEarlyAccess": null,
} satisfies AdminUpdateChapterRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AdminUpdateChapterRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


