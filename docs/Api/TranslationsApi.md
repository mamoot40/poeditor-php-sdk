# OpenAPI\Client\TranslationsApi

All URIs are relative to https://api.poeditor.com/v2, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**translationsAddPost()**](TranslationsApi.md#translationsAddPost) | **POST** /translations/add | Adds translations to project. If translation exists, it will not overwrite it. |
| [**translationsDeletePost()**](TranslationsApi.md#translationsDeletePost) | **POST** /translations/delete | Deletes translations from specified language. |
| [**translationsUpdatePost()**](TranslationsApi.md#translationsUpdatePost) | **POST** /translations/update | Updates existing translations. |


## `translationsAddPost()`

```php
translationsAddPost($api_token, $id, $language, $data): \OpenAPI\Client\Model\TranslationAddedResponse
```

Adds translations to project. If translation exists, it will not overwrite it.

Add Translations

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TranslationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$language = 'language_example'; // string | The language code
$data = 'data_example'; // string | JSON format

try {
    $result = $apiInstance->translationsAddPost($api_token, $id, $language, $data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TranslationsApi->translationsAddPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **language** | **string**| The language code | |
| **data** | **string**| JSON format | |

### Return type

[**\OpenAPI\Client\Model\TranslationAddedResponse**](../Model/TranslationAddedResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `translationsDeletePost()`

```php
translationsDeletePost($api_token, $id, $language, $data): \OpenAPI\Client\Model\TranslationDeletedResponse
```

Deletes translations from specified language.

Delete Translations

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TranslationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$language = 'language_example'; // string | The language code
$data = 'data_example'; // string | JSON format

try {
    $result = $apiInstance->translationsDeletePost($api_token, $id, $language, $data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TranslationsApi->translationsDeletePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **language** | **string**| The language code | |
| **data** | **string**| JSON format | |

### Return type

[**\OpenAPI\Client\Model\TranslationDeletedResponse**](../Model/TranslationDeletedResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `translationsUpdatePost()`

```php
translationsUpdatePost($api_token, $id, $language, $data): \OpenAPI\Client\Model\TranslationUpdatedResponse
```

Updates existing translations.

Update Translations

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TranslationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$language = 'language_example'; // string | The language code
$data = 'data_example'; // string | JSON format

try {
    $result = $apiInstance->translationsUpdatePost($api_token, $id, $language, $data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TranslationsApi->translationsUpdatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **language** | **string**| The language code | |
| **data** | **string**| JSON format | |

### Return type

[**\OpenAPI\Client\Model\TranslationUpdatedResponse**](../Model/TranslationUpdatedResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
