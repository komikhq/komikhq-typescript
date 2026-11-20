
# GetHealthStatus200Response


## Properties

Name | Type
------------ | -------------
`status` | string
`timestamp` | Date
`database` | [GetHealthStatus200ResponseDatabase](GetHealthStatus200ResponseDatabase.md)
`bindings` | [GetHealthStatus200ResponseBindings](GetHealthStatus200ResponseBindings.md)
`nodeCompat` | [GetHealthStatus200ResponseNodeCompat](GetHealthStatus200ResponseNodeCompat.md)

## Example

```typescript
import type { GetHealthStatus200Response } from '@komikhq/komikhq-typescript'

// TODO: Update the object below with actual values
const example = {
  "status": ok,
  "timestamp": null,
  "database": null,
  "bindings": null,
  "nodeCompat": null,
} satisfies GetHealthStatus200Response

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as GetHealthStatus200Response
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


