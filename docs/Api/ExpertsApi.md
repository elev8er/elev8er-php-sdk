# Elev8er\PublicApi\ExpertsApi

All URIs are relative to https://apidev.elev8er.ai/public/api/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAvailability()**](ExpertsApi.md#createAvailability) | **POST** /experts/availability | Create an availability entry |
| [**createExpert()**](ExpertsApi.md#createExpert) | **POST** /experts | Create an expert |
| [**createSession()**](ExpertsApi.md#createSession) | **POST** /experts/sessions | Create a session |
| [**deleteAvailability()**](ExpertsApi.md#deleteAvailability) | **DELETE** /experts/availability/{id} | Delete an availability entry |
| [**deleteExpert()**](ExpertsApi.md#deleteExpert) | **DELETE** /experts/{id} | Delete an expert |
| [**deleteSession()**](ExpertsApi.md#deleteSession) | **DELETE** /experts/sessions/{id} | Delete a session |
| [**getAvailability()**](ExpertsApi.md#getAvailability) | **GET** /experts/availability/{id} | Get an availability entry |
| [**getExpert()**](ExpertsApi.md#getExpert) | **GET** /experts/{id} | Get an expert by id |
| [**getExpertAvailability()**](ExpertsApi.md#getExpertAvailability) | **GET** /experts/{expertId}/availability | Get an expert&#39;s availability |
| [**getSession()**](ExpertsApi.md#getSession) | **GET** /experts/sessions/{id} | Get a session |
| [**listExpertSessions()**](ExpertsApi.md#listExpertSessions) | **GET** /experts/{expertId}/sessions | List sessions for an expert |
| [**listExperts()**](ExpertsApi.md#listExperts) | **GET** /experts | List experts |
| [**listSessions()**](ExpertsApi.md#listSessions) | **GET** /experts/sessions | List sessions |
| [**setExpertAvailability()**](ExpertsApi.md#setExpertAvailability) | **PUT** /experts/{expertId}/availability | Replace an expert&#39;s availability |
| [**updateAvailability()**](ExpertsApi.md#updateAvailability) | **PUT** /experts/availability/{id} | Update an availability entry |
| [**updateExpert()**](ExpertsApi.md#updateExpert) | **PUT** /experts/{id} | Update an expert |
| [**updateSession()**](ExpertsApi.md#updateSession) | **PUT** /experts/sessions/{id} | Update a session |
| [**updateSessionStatus()**](ExpertsApi.md#updateSessionStatus) | **PATCH** /experts/sessions/{id}/status | Update a session&#39;s status |


## `createAvailability()`

```php
createAvailability($body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Create an availability entry

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->createAvailability($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->createAvailability: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `createExpert()`

```php
createExpert($request_body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Create an expert

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request_body = NULL; // array<string,mixed>

try {
    $result = $apiInstance->createExpert($request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->createExpert: ', $e->getMessage(), PHP_EOL;
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

## `createSession()`

```php
createSession($body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Create a session

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->createSession($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->createSession: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `deleteAvailability()`

```php
deleteAvailability($id)
```

Delete an availability entry

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteAvailability($id);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->deleteAvailability: ', $e->getMessage(), PHP_EOL;
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
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteExpert()`

```php
deleteExpert($id)
```

Delete an expert

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteExpert($id);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->deleteExpert: ', $e->getMessage(), PHP_EOL;
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

## `deleteSession()`

```php
deleteSession($id)
```

Delete a session

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteSession($id);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->deleteSession: ', $e->getMessage(), PHP_EOL;
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
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAvailability()`

```php
getAvailability($id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Get an availability entry

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getAvailability($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->getAvailability: ', $e->getMessage(), PHP_EOL;
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

## `getExpert()`

```php
getExpert($id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Get an expert by id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getExpert($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->getExpert: ', $e->getMessage(), PHP_EOL;
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

## `getExpertAvailability()`

```php
getExpertAvailability($expert_id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Get an expert's availability

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$expert_id = 'expert_id_example'; // string

try {
    $result = $apiInstance->getExpertAvailability($expert_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->getExpertAvailability: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **expert_id** | **string**|  | |

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

## `getSession()`

```php
getSession($id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Get a session

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getSession($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->getSession: ', $e->getMessage(), PHP_EOL;
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

## `listExpertSessions()`

```php
listExpertSessions($expert_id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

List sessions for an expert

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$expert_id = 'expert_id_example'; // string

try {
    $result = $apiInstance->listExpertSessions($expert_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->listExpertSessions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **expert_id** | **string**|  | |

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

## `listExperts()`

```php
listExperts($page, $limit, $search): \Elev8er\PublicApi\Model\SuccessEnvelope
```

List experts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | 1-based page number.
$limit = 20; // int | Items per page (max 100).
$search = 'search_example'; // string | Free-text search filter.

try {
    $result = $apiInstance->listExperts($page, $limit, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->listExperts: ', $e->getMessage(), PHP_EOL;
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

## `listSessions()`

```php
listSessions($page, $limit): \Elev8er\PublicApi\Model\SuccessEnvelope
```

List sessions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | 1-based page number.
$limit = 20; // int | Items per page (max 100).

try {
    $result = $apiInstance->listSessions($page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->listSessions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| 1-based page number. | [optional] [default to 1] |
| **limit** | **int**| Items per page (max 100). | [optional] [default to 20] |

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

## `setExpertAvailability()`

```php
setExpertAvailability($expert_id, $body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Replace an expert's availability

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$expert_id = 'expert_id_example'; // string
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->setExpertAvailability($expert_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->setExpertAvailability: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **expert_id** | **string**|  | |
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

## `updateAvailability()`

```php
updateAvailability($id, $body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Update an availability entry

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->updateAvailability($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->updateAvailability: ', $e->getMessage(), PHP_EOL;
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

## `updateExpert()`

```php
updateExpert($id, $request_body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Update an expert

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$request_body = NULL; // array<string,mixed>

try {
    $result = $apiInstance->updateExpert($id, $request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->updateExpert: ', $e->getMessage(), PHP_EOL;
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

## `updateSession()`

```php
updateSession($id, $body): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Update a session

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->updateSession($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->updateSession: ', $e->getMessage(), PHP_EOL;
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

## `updateSessionStatus()`

```php
updateSessionStatus($id, $update_session_status_request): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Update a session's status

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\ExpertsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$update_session_status_request = new \Elev8er\PublicApi\Model\UpdateSessionStatusRequest(); // \Elev8er\PublicApi\Model\UpdateSessionStatusRequest

try {
    $result = $apiInstance->updateSessionStatus($id, $update_session_status_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpertsApi->updateSessionStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **update_session_status_request** | [**\Elev8er\PublicApi\Model\UpdateSessionStatusRequest**](../Model/UpdateSessionStatusRequest.md)|  | |

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
