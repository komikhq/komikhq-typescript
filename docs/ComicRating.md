
# ComicRating


## Properties

Name | Type
------------ | -------------
`averageRating` | number
`totalRatings` | number
`userRating` | number

## Example

```typescript
import type { ComicRating } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "averageRating": null,
  "totalRatings": null,
  "userRating": null,
} satisfies ComicRating

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ComicRating
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


