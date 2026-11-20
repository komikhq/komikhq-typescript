
# ReadingHistory


## Properties

Name | Type
------------ | -------------
`id` | string
`comicId` | string
`chapterId` | string
`lastPage` | number
`updatedAt` | Date
`comic` | [Comic](Comic.md)
`chapter` | [Chapter](Chapter.md)

## Example

```typescript
import type { ReadingHistory } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "comicId": null,
  "chapterId": null,
  "lastPage": null,
  "updatedAt": null,
  "comic": null,
  "chapter": null,
} satisfies ReadingHistory

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ReadingHistory
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


