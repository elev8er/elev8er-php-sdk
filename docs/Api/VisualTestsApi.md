# Elev8er\PublicApi\VisualTestsApi

All URIs are relative to https://apidev.elev8er.ai/public/api/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createVisualTest()**](VisualTestsApi.md#createVisualTest) | **POST** /visual-tests | Create a visual test |
| [**createVisualTestVersion()**](VisualTestsApi.md#createVisualTestVersion) | **POST** /visual-tests/{id}/versions | Create a new version of a visual test |
| [**deleteVisualTest()**](VisualTestsApi.md#deleteVisualTest) | **DELETE** /visual-tests/{id} | Delete a visual test |
| [**getVisualTest()**](VisualTestsApi.md#getVisualTest) | **GET** /visual-tests/{id} | Get a visual test by id |
| [**getVisualTestVersion()**](VisualTestsApi.md#getVisualTestVersion) | **GET** /visual-tests/{id}/versions/{versionId} | Get a specific visual test version |
| [**listVisualTestVersions()**](VisualTestsApi.md#listVisualTestVersions) | **GET** /visual-tests/{id}/versions | List versions of a visual test |
| [**listVisualTests()**](VisualTestsApi.md#listVisualTests) | **GET** /visual-tests | List visual tests |
| [**rollbackVisualTestVersion()**](VisualTestsApi.md#rollbackVisualTestVersion) | **POST** /visual-tests/{id}/versions/{versionId}/rollback | Roll a visual test back to a specific version |
| [**updateVisualTest()**](VisualTestsApi.md#updateVisualTest) | **PUT** /visual-tests/{id} | Update a visual test |
| [**updateVisualTestVersion()**](VisualTestsApi.md#updateVisualTestVersion) | **PUT** /visual-tests/{id}/versions/{versionId} | Update a specific visual test version |


## `createVisualTest()`

```php
createVisualTest($request_body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Create a visual test

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\VisualTestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request_body = NULL; // array<string,mixed>

try {
    $result = $apiInstance->createVisualTest($request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VisualTestsApi->createVisualTest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request_body** | [**array<string,mixed>**](../Model/mixed.md)|  | |

### Return type

[**\Elev8er\PublicApi\Model\SuccessEnvelope**](../Model/SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createVisualTestVersion()`

```php
createVisualTestVersion($id, $body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Create a new version of a visual test

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\VisualTestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->createVisualTestVersion($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VisualTestsApi->createVisualTestVersion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **body** | **object**|  | |

### Return type

[**\Elev8er\PublicApi\Model\SuccessEnvelope**](../Model/SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteVisualTest()`

```php
deleteVisualTest($id)
```

Delete a visual test

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\VisualTestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteVisualTest($id);
} catch (Exception $e) {
    echo 'Exception when calling VisualTestsApi->deleteVisualTest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVisualTest()`

```php
getVisualTest($id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Get a visual test by id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\VisualTestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getVisualTest($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VisualTestsApi->getVisualTest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\Elev8er\PublicApi\Model\SuccessEnvelope**](../Model/SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVisualTestVersion()`

```php
getVisualTestVersion($id, $version_id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Get a specific visual test version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\VisualTestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$version_id = 'version_id_example'; // string

try {
    $result = $apiInstance->getVisualTestVersion($id, $version_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VisualTestsApi->getVisualTestVersion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **version_id** | **string**|  | |

### Return type

[**\Elev8er\PublicApi\Model\SuccessEnvelope**](../Model/SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listVisualTestVersions()`

```php
listVisualTestVersions($id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

List versions of a visual test

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\VisualTestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->listVisualTestVersions($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VisualTestsApi->listVisualTestVersions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\Elev8er\PublicApi\Model\SuccessEnvelope**](../Model/SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listVisualTests()`

```php
listVisualTests($page, $limit, $search): \Elev8er\PublicApi\Model\SuccessEnvelope
```

List visual tests

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\VisualTestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | 1-based page number.
$limit = 20; // int | Items per page (max 100).
$search = 'search_example'; // string | Free-text search filter.

try {
    $result = $apiInstance->listVisualTests($page, $limit, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VisualTestsApi->listVisualTests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| 1-based page number. | [optional] [default to 1] |
| **limit** | **int**| Items per page (max 100). | [optional] [default to 20] |
| **search** | **string**| Free-text search filter. | [optional] |

### Return type

[**\Elev8er\PublicApi\Model\SuccessEnvelope**](../Model/SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rollbackVisualTestVersion()`

```php
rollbackVisualTestVersion($id, $version_id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Roll a visual test back to a specific version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\VisualTestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$version_id = 'version_id_example'; // string

try {
    $result = $apiInstance->rollbackVisualTestVersion($id, $version_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VisualTestsApi->rollbackVisualTestVersion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **version_id** | **string**|  | |

### Return type

[**\Elev8er\PublicApi\Model\SuccessEnvelope**](../Model/SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateVisualTest()`

```php
updateVisualTest($id, $request_body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Update a visual test

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\VisualTestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$request_body = NULL; // array<string,mixed>

try {
    $result = $apiInstance->updateVisualTest($id, $request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VisualTestsApi->updateVisualTest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **request_body** | [**array<string,mixed>**](../Model/mixed.md)|  | |

### Return type

[**\Elev8er\PublicApi\Model\SuccessEnvelope**](../Model/SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateVisualTestVersion()`

```php
updateVisualTestVersion($id, $version_id, $body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Update a specific visual test version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\VisualTestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$version_id = 'version_id_example'; // string
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->updateVisualTestVersion($id, $version_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VisualTestsApi->updateVisualTestVersion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **version_id** | **string**|  | |
| **body** | **object**|  | |

### Return type

[**\Elev8er\PublicApi\Model\SuccessEnvelope**](../Model/SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
