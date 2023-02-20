# OpenAPI\Client\LanguagesApi

All URIs are relative to https://api.poeditor.com/v2, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**languagesAddPost()**](LanguagesApi.md#languagesAddPost) | **POST** /languages/add | Adds a new language to project. |
| [**languagesAvailablePost()**](LanguagesApi.md#languagesAvailablePost) | **POST** /languages/available | Returns project languages, percentage of translation done for each and the datetime (UTC - ISO 8601) when the last change was made. |
| [**languagesDeletePost()**](LanguagesApi.md#languagesDeletePost) | **POST** /languages/delete | Deletes existing language from project. |
| [**languagesListPost()**](LanguagesApi.md#languagesListPost) | **POST** /languages/list | Returns project languages, percentage of translation done for each and the datetime (UTC - ISO 8601) when the last change was made. |
| [**languagesUpdatePost()**](LanguagesApi.md#languagesUpdatePost) | **POST** /languages/update | Inserts / overwrites translations. |


## `languagesAddPost()`

```php
languagesAddPost($api_token, $id, $language): \OpenAPI\Client\Model\Response
```

Adds a new language to project.

Add Language to Project

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LanguagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$language = 'language_example'; // string

try {
    $result = $apiInstance->languagesAddPost($api_token, $id, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LanguagesApi->languagesAddPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **language** | **string**|  | |

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

## `languagesAvailablePost()`

```php
languagesAvailablePost($api_token, $id): \OpenAPI\Client\Model\LanguagesListShortResponse
```

Returns project languages, percentage of translation done for each and the datetime (UTC - ISO 8601) when the last change was made.

List Languages

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LanguagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int

try {
    $result = $apiInstance->languagesAvailablePost($api_token, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LanguagesApi->languagesAvailablePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\LanguagesListShortResponse**](../Model/LanguagesListShortResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `languagesDeletePost()`

```php
languagesDeletePost($api_token, $id, $language): \OpenAPI\Client\Model\Response
```

Deletes existing language from project.

Delete Language from Project

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LanguagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$language = 'language_example'; // string

try {
    $result = $apiInstance->languagesDeletePost($api_token, $id, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LanguagesApi->languagesDeletePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **language** | **string**|  | |

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

## `languagesListPost()`

```php
languagesListPost($api_token, $id): \OpenAPI\Client\Model\LanguagesListLongResponse
```

Returns project languages, percentage of translation done for each and the datetime (UTC - ISO 8601) when the last change was made.

List Languages

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LanguagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int

try {
    $result = $apiInstance->languagesListPost($api_token, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LanguagesApi->languagesListPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\LanguagesListLongResponse**](../Model/LanguagesListLongResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `languagesUpdatePost()`

```php
languagesUpdatePost($api_token, $id, $language, $data, $fuzzy_trigger): \OpenAPI\Client\Model\TranslationsShortResponse
```

Inserts / overwrites translations.

Update Project Language

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\LanguagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$language = 'language_example'; // string | The language code
$data = 'data_example'; // string | JSON format
$fuzzy_trigger = 56; // int | Set it to 1 to mark corresponding translations from the other languages as fuzzy for the updated values

try {
    $result = $apiInstance->languagesUpdatePost($api_token, $id, $language, $data, $fuzzy_trigger);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LanguagesApi->languagesUpdatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **language** | **string**| The language code | |
| **data** | **string**| JSON format | |
| **fuzzy_trigger** | **int**| Set it to 1 to mark corresponding translations from the other languages as fuzzy for the updated values | [optional] |

### Return type

[**\OpenAPI\Client\Model\TranslationsShortResponse**](../Model/TranslationsShortResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
