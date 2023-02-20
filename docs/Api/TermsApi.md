# OpenAPI\Client\TermsApi

All URIs are relative to https://api.poeditor.com/v2, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**termsAddCommentPost()**](TermsApi.md#termsAddCommentPost) | **POST** /terms/add_comment | Adds comments to existing terms. |
| [**termsAddPost()**](TermsApi.md#termsAddPost) | **POST** /terms/add | Adds terms to project. |
| [**termsDeletePost()**](TermsApi.md#termsDeletePost) | **POST** /terms/delete | Deletes terms from project. |
| [**termsListPost()**](TermsApi.md#termsListPost) | **POST** /terms/list | Returns project&#39;s terms and translations if the argument language is provided. |
| [**termsUpdatePost()**](TermsApi.md#termsUpdatePost) | **POST** /terms/update | Updates project terms. Lets you change the text, context, reference, plural and tags. |


## `termsAddCommentPost()`

```php
termsAddCommentPost($api_token, $id, $data): \OpenAPI\Client\Model\TermAddCommentResponse
```

Adds comments to existing terms.

Add Comment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TermsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$data = 'data_example'; // string | JSON format

try {
    $result = $apiInstance->termsAddCommentPost($api_token, $id, $data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TermsApi->termsAddCommentPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **data** | **string**| JSON format | |

### Return type

[**\OpenAPI\Client\Model\TermAddCommentResponse**](../Model/TermAddCommentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `termsAddPost()`

```php
termsAddPost($api_token, $id, $data): \OpenAPI\Client\Model\TermAddedResponse
```

Adds terms to project.

Add Terms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TermsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$data = 'data_example'; // string | JSON format

try {
    $result = $apiInstance->termsAddPost($api_token, $id, $data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TermsApi->termsAddPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **data** | **string**| JSON format | |

### Return type

[**\OpenAPI\Client\Model\TermAddedResponse**](../Model/TermAddedResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `termsDeletePost()`

```php
termsDeletePost($api_token, $id, $data): \OpenAPI\Client\Model\TermDeletedResponse
```

Deletes terms from project.

Delete Terms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TermsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$data = 'data_example'; // string | JSON format

try {
    $result = $apiInstance->termsDeletePost($api_token, $id, $data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TermsApi->termsDeletePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **data** | **string**| JSON format | |

### Return type

[**\OpenAPI\Client\Model\TermDeletedResponse**](../Model/TermDeletedResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `termsListPost()`

```php
termsListPost($api_token, $id, $language): \OpenAPI\Client\Model\TermsListFullResponse
```

Returns project's terms and translations if the argument language is provided.

List Project Terms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TermsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$language = 'language_example'; // string | The language code

try {
    $result = $apiInstance->termsListPost($api_token, $id, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TermsApi->termsListPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **language** | **string**| The language code | [optional] |

### Return type

[**\OpenAPI\Client\Model\TermsListFullResponse**](../Model/TermsListFullResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `termsUpdatePost()`

```php
termsUpdatePost($api_token, $id, $data, $fuzzy_trigger): \OpenAPI\Client\Model\TermUpdatedResponse
```

Updates project terms. Lets you change the text, context, reference, plural and tags.

Update Terms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TermsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$data = 'data_example'; // string | JSON format
$fuzzy_trigger = 56; // int | Set it to 1 to mark corresponding translations from the other languages as fuzzy for the updated values

try {
    $result = $apiInstance->termsUpdatePost($api_token, $id, $data, $fuzzy_trigger);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TermsApi->termsUpdatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **data** | **string**| JSON format | |
| **fuzzy_trigger** | **int**| Set it to 1 to mark corresponding translations from the other languages as fuzzy for the updated values | [optional] |

### Return type

[**\OpenAPI\Client\Model\TermUpdatedResponse**](../Model/TermUpdatedResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
