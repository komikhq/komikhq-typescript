# UsersApi

All URIs are relative to *https://nitro.komikhq.dpdns.org*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteOwnAccount**](UsersApi.md#deleteownaccountoperation) | **DELETE** /users/profile | Delete own account |
| [**getUserProfile**](UsersApi.md#getuserprofile) | **GET** /users/profile | Get current user profile |
| [**uploadUserAvatar**](UsersApi.md#uploaduseravatar) | **POST** /users/avatar | Upload profile avatar image |



## deleteOwnAccount

> SuccessResponse deleteOwnAccount(deleteOwnAccountRequest)

Delete own account

Permanently deletes the authenticated user\&#39;s account with confirmation password or matching email.

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '@komikhq/komikhq-typescript';
import type { DeleteOwnAccountOperationRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  const body = {
    // DeleteOwnAccountRequest (optional)
    deleteOwnAccountRequest: ...,
  } satisfies DeleteOwnAccountOperationRequest;

  try {
    const data = await api.deleteOwnAccount(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **deleteOwnAccountRequest** | [DeleteOwnAccountRequest](DeleteOwnAccountRequest.md) |  | [Optional] |

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account deleted successfully. |  -  |
| **400** | Verification failed. |  -  |
| **401** | Unauthorized. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getUserProfile

> AdminUpdateUser200Response getUserProfile()

Get current user profile

Returns profile details and credential password status for the authenticated user.

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '@komikhq/komikhq-typescript';
import type { GetUserProfileRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  try {
    const data = await api.getUserProfile();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AdminUpdateUser200Response**](AdminUpdateUser200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User profile retrieved successfully. |  -  |
| **401** | Unauthorized. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## uploadUserAvatar

> UploadUserAvatar200Response uploadUserAvatar(file)

Upload profile avatar image

Uploads an image file to R2 storage and updates the user\&#39;s avatar URL.

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '@komikhq/komikhq-typescript';
import type { UploadUserAvatarRequest } from '@komikhq/komikhq-typescript';

async function example() {
  console.log("🚀 Testing @komikhq/komikhq-typescript SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: SessionCookie
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: BearerToken
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  const body = {
    // Blob | Image file to upload
    file: BINARY_DATA_HERE,
  } satisfies UploadUserAvatarRequest;

  try {
    const data = await api.uploadUserAvatar(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **file** | `Blob` | Image file to upload | [Defaults to `undefined`] |

### Return type

[**UploadUserAvatar200Response**](UploadUserAvatar200Response.md)

### Authorization

[SessionCookie](../README.md#SessionCookie), [BearerToken](../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Avatar updated successfully. |  -  |
| **400** | Invalid file. |  -  |
| **401** | Unauthorized. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

