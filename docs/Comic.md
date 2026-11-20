
# Comic


## Properties

Name | Type
------------ | -------------
`id` | string
`title` | string
`slug` | string
`synopsis` | string
`coverUrl` | string
`bannerUrl` | string
`type` | string
`status` | string
`accessTier` | string
`totalChapters` | number
`totalViews` | number
`createdAt` | Date
`updatedAt` | Date
`genres` | [Array&lt;ComicGenresInner&gt;](ComicGenresInner.md)

## Example

```typescript
import type { Comic } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "title": null,
  "slug": null,
  "synopsis": null,
  "coverUrl": null,
  "bannerUrl": null,
  "type": null,
  "status": null,
  "accessTier": null,
  "totalChapters": null,
  "totalViews": null,
  "createdAt": null,
  "updatedAt": null,
  "genres": null,
} satisfies Comic

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Comic
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


