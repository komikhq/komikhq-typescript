
# AdminUpdateUserRequest


## Properties

Name | Type
------------ | -------------
`name` | string
`email` | string
`role` | string
`password` | string

## Example

```typescript
import type { AdminUpdateUserRequest } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "name": null,
  "email": null,
  "role": null,
  "password": null,
} satisfies AdminUpdateUserRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AdminUpdateUserRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


