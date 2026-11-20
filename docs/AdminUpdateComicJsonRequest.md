
# AdminUpdateComicJsonRequest


## Properties

Name | Type
------------ | -------------
`title` | string
`slug` | string
`synopsis` | string
`coverUrl` | string
`bannerUrl` | string
`type` | string
`status` | string
`accessTier` | string
`genreIds` | Array&lt;string&gt;

## Example

```typescript
import type { AdminUpdateComicJsonRequest } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "title": null,
  "slug": null,
  "synopsis": null,
  "coverUrl": null,
  "bannerUrl": null,
  "type": null,
  "status": null,
  "accessTier": null,
  "genreIds": null,
} satisfies AdminUpdateComicJsonRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AdminUpdateComicJsonRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


