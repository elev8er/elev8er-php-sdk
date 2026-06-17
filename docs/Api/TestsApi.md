# Elev8er\PublicApi\TestsApi

All URIs are relative to https://apidev.elev8er.ai/public/api/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTest()**](TestsApi.md#createTest) | **POST** /tests | Create a test |
| [**createTestVersion()**](TestsApi.md#createTestVersion) | **POST** /tests/{id}/versions | Create a new version of a test |
| [**deleteTest()**](TestsApi.md#deleteTest) | **DELETE** /tests/{id} | Delete a test |
| [**getTest()**](TestsApi.md#getTest) | **GET** /tests/{id} | Get a test by id |
| [**getTestVersion()**](TestsApi.md#getTestVersion) | **GET** /tests/{id}/versions/{versionId} | Get a specific test version |
| [**listTestVersions()**](TestsApi.md#listTestVersions) | **GET** /tests/{id}/versions | List versions of a test |
| [**listTests()**](TestsApi.md#listTests) | **GET** /tests | List tests |
| [**rollbackTestVersion()**](TestsApi.md#rollbackTestVersion) | **POST** /tests/{id}/versions/{versionId}/rollback | Roll a test back to a specific version |
| [**updateTest()**](TestsApi.md#updateTest) | **PUT** /tests/{id} | Update a test |
| [**updateTestVersion()**](TestsApi.md#updateTestVersion) | **PUT** /tests/{id}/versions/{versionId} | Update a specific test version |


## `createTest()`

```php
createTest($request_body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Create a test

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\TestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request_body = NULL; // array<string,mixed>

try {
    $result = $apiInstance->createTest($request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TestsApi->createTest: ', $e->getMessage(), PHP_EOL;
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

## `createTestVersion()`

```php
createTestVersion($id, $body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Create a new version of a test

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\TestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->createTestVersion($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TestsApi->createTestVersion: ', $e->getMessage(), PHP_EOL;
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

## `deleteTest()`

```php
deleteTest($id)
```

Delete a test

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\TestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteTest($id);
} catch (Exception $e) {
    echo 'Exception when calling TestsApi->deleteTest: ', $e->getMessage(), PHP_EOL;
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

## `getTest()`

```php
getTest($id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Get a test by id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\TestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getTest($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TestsApi->getTest: ', $e->getMessage(), PHP_EOL;
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

## `getTestVersion()`

```php
getTestVersion($id, $version_id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Get a specific test version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\TestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$version_id = 'version_id_example'; // string

try {
    $result = $apiInstance->getTestVersion($id, $version_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TestsApi->getTestVersion: ', $e->getMessage(), PHP_EOL;
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

## `listTestVersions()`

```php
listTestVersions($id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

List versions of a test

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\TestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->listTestVersions($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TestsApi->listTestVersions: ', $e->getMessage(), PHP_EOL;
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

## `listTests()`

```php
listTests($page, $limit, $search): \Elev8er\PublicApi\Model\SuccessEnvelope
```

List tests

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\TestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | 1-based page number.
$limit = 20; // int | Items per page (max 100).
$search = 'search_example'; // string | Free-text search filter.

try {
    $result = $apiInstance->listTests($page, $limit, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TestsApi->listTests: ', $e->getMessage(), PHP_EOL;
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

## `rollbackTestVersion()`

```php
rollbackTestVersion($id, $version_id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Roll a test back to a specific version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\TestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$version_id = 'version_id_example'; // string

try {
    $result = $apiInstance->rollbackTestVersion($id, $version_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TestsApi->rollbackTestVersion: ', $e->getMessage(), PHP_EOL;
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

## `updateTest()`

```php
updateTest($id, $request_body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Update a test

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\TestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$request_body = NULL; // array<string,mixed>

try {
    $result = $apiInstance->updateTest($id, $request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TestsApi->updateTest: ', $e->getMessage(), PHP_EOL;
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

## `updateTestVersion()`

```php
updateTestVersion($id, $version_id, $body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Update a specific test version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\TestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$version_id = 'version_id_example'; // string
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->updateTestVersion($id, $version_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TestsApi->updateTestVersion: ', $e->getMessage(), PHP_EOL;
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
