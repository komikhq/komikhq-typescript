
# Bookmark


## Properties

Name | Type
------------ | -------------
`id` | string
`comicId` | string
`userId` | string
`createdAt` | Date
`comic` | [Comic](Comic.md)

## Example

```typescript
import type { Bookmark } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "comicId": null,
  "userId": null,
  "createdAt": null,
  "comic": null,
} satisfies Bookmark

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Bookmark
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


