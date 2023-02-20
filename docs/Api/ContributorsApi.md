# OpenAPI\Client\ContributorsApi

All URIs are relative to https://api.poeditor.com/v2, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contributorsAddPost()**](ContributorsApi.md#contributorsAddPost) | **POST** /contributors/add | Adds a contributor to a project language or an administrator to a project. |
| [**contributorsListPost()**](ContributorsApi.md#contributorsListPost) | **POST** /contributors/list | Returns the list of contributors from your projects. |
| [**contributorsRemovePost()**](ContributorsApi.md#contributorsRemovePost) | **POST** /contributors/remove | Removes a contributor from a project language or an admin from a project, if the language is not specified. |


## `contributorsAddPost()`

```php
contributorsAddPost($api_token, $id, $name, $email, $language, $admin): \OpenAPI\Client\Model\Response
```

Adds a contributor to a project language or an administrator to a project.

Add Contributor

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ContributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 'id_example'; // string | The id of project
$name = 'name_example'; // string | The name of contributor
$email = 'email_example'; // string | The email of contributor
$language = 'language_example'; // string | The language code (Required if adding a contributor)
$admin = 56; // int | Set it to 1 for adding as administrator

try {
    $result = $apiInstance->contributorsAddPost($api_token, $id, $name, $email, $language, $admin);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContributorsApi->contributorsAddPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **string**| The id of project | |
| **name** | **string**| The name of contributor | |
| **email** | **string**| The email of contributor | |
| **language** | **string**| The language code (Required if adding a contributor) | [optional] |
| **admin** | **int**| Set it to 1 for adding as administrator | [optional] |

### Return type

[**\OpenAPI\Client\Model\Response**](../Model/Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `contributorsListPost()`

```php
contributorsListPost($api_token, $id, $language): \OpenAPI\Client\Model\ContributorsListResponse
```

Returns the list of contributors from your projects.

List Contributors

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ContributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 'id_example'; // string | The id of project (Optional, unless language is set. Then, it becomes required)
$language = 'language_example'; // string | The language code

try {
    $result = $apiInstance->contributorsListPost($api_token, $id, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContributorsApi->contributorsListPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **string**| The id of project (Optional, unless language is set. Then, it becomes required) | [optional] |
| **language** | **string**| The language code | [optional] |

### Return type

[**\OpenAPI\Client\Model\ContributorsListResponse**](../Model/ContributorsListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `contributorsRemovePost()`

```php
contributorsRemovePost($api_token, $id, $email, $language): \OpenAPI\Client\Model\Response
```

Removes a contributor from a project language or an admin from a project, if the language is not specified.

Remove Contributor

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ContributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 'id_example'; // string | The id of project
$email = 'email_example'; // string | The email of contributor
$language = 'language_example'; // string | The language code (Required if removing a contributor from a certain language)

try {
    $result = $apiInstance->contributorsRemovePost($api_token, $id, $email, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContributorsApi->contributorsRemovePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **string**| The id of project | |
| **email** | **string**| The email of contributor | |
| **language** | **string**| The language code (Required if removing a contributor from a certain language) | [optional] |

### Return type

[**\OpenAPI\Client\Model\Response**](../Model/Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
