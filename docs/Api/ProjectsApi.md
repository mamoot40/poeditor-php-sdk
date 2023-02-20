# OpenAPI\Client\ProjectsApi

All URIs are relative to https://api.poeditor.com/v2, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**projectsAddPost()**](ProjectsApi.md#projectsAddPost) | **POST** /projects/add | Creates a new project. Returns project details (if successful) |
| [**projectsDeletePost()**](ProjectsApi.md#projectsDeletePost) | **POST** /projects/delete | Deletes the project from the account. You must be the owner of the project. |
| [**projectsExportPost()**](ProjectsApi.md#projectsExportPost) | **POST** /projects/export | Returns the link of the file (expires after 10 minutes). The settings inherited from the project will be the ones at the time of the download. |
| [**projectsListPost()**](ProjectsApi.md#projectsListPost) | **POST** /projects/list | Returns the list of projects owned by user. |
| [**projectsSyncPost()**](ProjectsApi.md#projectsSyncPost) | **POST** /projects/sync | Syncs your project with the array you send (terms that are not found in the JSON object will be deleted from project and the new ones added). Please use with caution. If wrong data is sent, existing terms and their translations might be irreversibly lost. |
| [**projectsUpdatePost()**](ProjectsApi.md#projectsUpdatePost) | **POST** /projects/update | Updates project settings (name, description, reference language, fallback language). If optional parameters are not sent, their respective fields are not updated. |
| [**projectsUploadPost()**](ProjectsApi.md#projectsUploadPost) | **POST** /projects/upload | Updates terms / translations - No more than one request every 30 seconds. |
| [**projectsViewPost()**](ProjectsApi.md#projectsViewPost) | **POST** /projects/view | Returns projects details |


## `projectsAddPost()`

```php
projectsAddPost($api_token, $name, $description): \OpenAPI\Client\Model\ProjectViewResponse
```

Creates a new project. Returns project details (if successful)

Add Project

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$name = 'name_example'; // string
$description = 'description_example'; // string

try {
    $result = $apiInstance->projectsAddPost($api_token, $name, $description);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectsApi->projectsAddPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **name** | **string**|  | |
| **description** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProjectViewResponse**](../Model/ProjectViewResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectsDeletePost()`

```php
projectsDeletePost($api_token, $id): \OpenAPI\Client\Model\Response
```

Deletes the project from the account. You must be the owner of the project.

Delete Project

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int

try {
    $result = $apiInstance->projectsDeletePost($api_token, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectsApi->projectsDeletePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |

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

## `projectsExportPost()`

```php
projectsExportPost($api_token, $id, $language, $type, $filters, $order, $tags, $options): \OpenAPI\Client\Model\ProjectExportResponse
```

Returns the link of the file (expires after 10 minutes). The settings inherited from the project will be the ones at the time of the download.

Export

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$language = 'language_example'; // string
$type = 'type_example'; // string
$filters = 'filters_example'; // string
$order = 'order_example'; // string
$tags = 'tags_example'; // string
$options = 'options_example'; // string

try {
    $result = $apiInstance->projectsExportPost($api_token, $id, $language, $type, $filters, $order, $tags, $options);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectsApi->projectsExportPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **language** | **string**|  | |
| **type** | **string**|  | |
| **filters** | **string**|  | [optional] |
| **order** | **string**|  | [optional] |
| **tags** | **string**|  | [optional] |
| **options** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProjectExportResponse**](../Model/ProjectExportResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectsListPost()`

```php
projectsListPost($api_token): \OpenAPI\Client\Model\ProjectListResponse
```

Returns the list of projects owned by user.

List Projects

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string

try {
    $result = $apiInstance->projectsListPost($api_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectsApi->projectsListPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ProjectListResponse**](../Model/ProjectListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectsSyncPost()`

```php
projectsSyncPost($api_token, $id, $data): \OpenAPI\Client\Model\ProjectSyncResponse
```

Syncs your project with the array you send (terms that are not found in the JSON object will be deleted from project and the new ones added). Please use with caution. If wrong data is sent, existing terms and their translations might be irreversibly lost.

Sync Terms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$data = 'data_example'; // string

try {
    $result = $apiInstance->projectsSyncPost($api_token, $id, $data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectsApi->projectsSyncPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **data** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ProjectSyncResponse**](../Model/ProjectSyncResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectsUpdatePost()`

```php
projectsUpdatePost($api_token, $id, $name, $description, $reference_language, $fallback_language): \OpenAPI\Client\Model\ProjectViewResponse
```

Updates project settings (name, description, reference language, fallback language). If optional parameters are not sent, their respective fields are not updated.

Update Project Settings

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int
$name = 'name_example'; // string
$description = 'description_example'; // string
$reference_language = 'reference_language_example'; // string
$fallback_language = 'fallback_language_example'; // string

try {
    $result = $apiInstance->projectsUpdatePost($api_token, $id, $name, $description, $reference_language, $fallback_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectsApi->projectsUpdatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |
| **name** | **string**|  | [optional] |
| **description** | **string**|  | [optional] |
| **reference_language** | **string**|  | [optional] |
| **fallback_language** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProjectViewResponse**](../Model/ProjectViewResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectsUploadPost()`

```php
projectsUploadPost($updating, $file, $api_token, $id, $language, $overwrite, $sync_terms, $tags, $read_from_source, $fuzzy_trigger): \OpenAPI\Client\Model\ProjectUploadResponse
```

Updates terms / translations - No more than one request every 30 seconds.

Upload

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$updating = 'updating_example'; // string
$file = "/path/to/file.txt"; // \SplFileObject | Uploaded file (.po, .xls or any of the supported file formats)
$api_token = 'api_token_example'; // string
$id = 56; // int
$language = 'language_example'; // string | The language code (Required only if `updating` is terms_translations or translations)
$overwrite = 56; // int | Set it to 1 if you want to overwrite translations
$sync_terms = 56; // int | Set it to 1 if you want to sync your terms (terms that are not found in the uploaded file will be deleted from project and the new ones added). Ignored if `updating` = translations.
$tags = 'tags_example'; // string | Add tags to the project terms; available when updating terms or terms_translations; you can use the following keys: \\\"all\\\" - for the all the imported terms, \\\"new\\\" - for the terms which arent already in the project, \\\"obsolete\\\" - for the terms which are in the project but not in the imported file and \\\"overwritten_translations\\\" - for the terms for which translations change
$read_from_source = 56; // int | For .xliff format only - set it to 1 if you want to import translations from the source tag
$fuzzy_trigger = 56; // int | Set it to 1 to mark corresponding translations from the other languages as fuzzy for the updated values

try {
    $result = $apiInstance->projectsUploadPost($updating, $file, $api_token, $id, $language, $overwrite, $sync_terms, $tags, $read_from_source, $fuzzy_trigger);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectsApi->projectsUploadPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updating** | **string**|  | |
| **file** | **\SplFileObject****\SplFileObject**| Uploaded file (.po, .xls or any of the supported file formats) | |
| **api_token** | **string**|  | [optional] |
| **id** | **int**|  | [optional] |
| **language** | **string**| The language code (Required only if &#x60;updating&#x60; is terms_translations or translations) | [optional] |
| **overwrite** | **int**| Set it to 1 if you want to overwrite translations | [optional] |
| **sync_terms** | **int**| Set it to 1 if you want to sync your terms (terms that are not found in the uploaded file will be deleted from project and the new ones added). Ignored if &#x60;updating&#x60; &#x3D; translations. | [optional] |
| **tags** | **string**| Add tags to the project terms; available when updating terms or terms_translations; you can use the following keys: \\\&quot;all\\\&quot; - for the all the imported terms, \\\&quot;new\\\&quot; - for the terms which arent already in the project, \\\&quot;obsolete\\\&quot; - for the terms which are in the project but not in the imported file and \\\&quot;overwritten_translations\\\&quot; - for the terms for which translations change | [optional] |
| **read_from_source** | **int**| For .xliff format only - set it to 1 if you want to import translations from the source tag | [optional] |
| **fuzzy_trigger** | **int**| Set it to 1 to mark corresponding translations from the other languages as fuzzy for the updated values | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProjectUploadResponse**](../Model/ProjectUploadResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectsViewPost()`

```php
projectsViewPost($api_token, $id): \OpenAPI\Client\Model\ProjectViewResponse
```

Returns projects details

View Project Details

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProjectsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 56; // int

try {
    $result = $apiInstance->projectsViewPost($api_token, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectsApi->projectsViewPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_token** | **string**|  | |
| **id** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\ProjectViewResponse**](../Model/ProjectViewResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
