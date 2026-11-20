
# AdminCreateApiTokenRequest


## Properties

Name | Type
------------ | -------------
`name` | string
`scopes` | Array&lt;string&gt;
`expiresInDays` | number

## Example

```typescript
import type { AdminCreateApiTokenRequest } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "name": null,
  "scopes": null,
  "expiresInDays": null,
} satisfies AdminCreateApiTokenRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AdminCreateApiTokenRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


