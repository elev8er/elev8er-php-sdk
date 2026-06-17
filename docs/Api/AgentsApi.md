# Elev8er\PublicApi\AgentsApi

All URIs are relative to https://apidev.elev8er.ai/public/api/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAgentChat()**](AgentsApi.md#createAgentChat) | **POST** /agents/{id}/chats | Start a new chat with an agent |
| [**getAgent()**](AgentsApi.md#getAgent) | **GET** /agents/{id} | Get an agent by id |
| [**listAgentChats()**](AgentsApi.md#listAgentChats) | **GET** /agents/{id}/chats | List chats for an agent |
| [**listAgents()**](AgentsApi.md#listAgents) | **GET** /agents | List agents |
| [**listChatMessages()**](AgentsApi.md#listChatMessages) | **GET** /agents/{id}/chats/{chatId}/messages | Get messages in a chat |
| [**sendChatMessage()**](AgentsApi.md#sendChatMessage) | **POST** /agents/{id}/chats/{chatId}/messages | Send a message to the agent and get its reply (non-streaming) |


## `createAgentChat()`

```php
createAgentChat($id, $create_agent_chat_request): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Start a new chat with an agent

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\AgentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$create_agent_chat_request = new \Elev8er\PublicApi\Model\CreateAgentChatRequest(); // \Elev8er\PublicApi\Model\CreateAgentChatRequest

try {
    $result = $apiInstance->createAgentChat($id, $create_agent_chat_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AgentsApi->createAgentChat: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **create_agent_chat_request** | [**\Elev8er\PublicApi\Model\CreateAgentChatRequest**](../Model/CreateAgentChatRequest.md)|  | [optional] |

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

## `getAgent()`

```php
getAgent($id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Get an agent by id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\AgentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getAgent($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AgentsApi->getAgent: ', $e->getMessage(), PHP_EOL;
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

## `listAgentChats()`

```php
listAgentChats($id): \Elev8er\PublicApi\Model\SuccessEnvelope
```

List chats for an agent

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\AgentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->listAgentChats($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AgentsApi->listAgentChats: ', $e->getMessage(), PHP_EOL;
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

## `listAgents()`

```php
listAgents($page, $limit): \Elev8er\PublicApi\Model\SuccessEnvelope
```

List agents

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\AgentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | 1-based page number.
$limit = 20; // int | Items per page (max 100).

try {
    $result = $apiInstance->listAgents($page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AgentsApi->listAgents: ', $e->getMessage(), PHP_EOL;
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

## `listChatMessages()`

```php
listChatMessages($id, $chat_id, $page, $limit): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Get messages in a chat

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\AgentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$chat_id = 'chat_id_example'; // string
$page = 1; // int | 1-based page number.
$limit = 20; // int | Items per page (max 100).

try {
    $result = $apiInstance->listChatMessages($id, $chat_id, $page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AgentsApi->listChatMessages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **chat_id** | **string**|  | |
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

## `sendChatMessage()`

```php
sendChatMessage($id, $chat_id, $chat_message_input): \Elev8er\PublicApi\Model\SuccessEnvelope
```

Send a message to the agent and get its reply (non-streaming)

Sends a user message to the agent and returns the agent's full reply in a single JSON response. Streaming is not exposed on the public API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Elev8er\PublicApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Elev8er\PublicApi\Api\AgentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$chat_id = 'chat_id_example'; // string
$chat_message_input = new \Elev8er\PublicApi\Model\ChatMessageInput(); // \Elev8er\PublicApi\Model\ChatMessageInput

try {
    $result = $apiInstance->sendChatMessage($id, $chat_id, $chat_message_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AgentsApi->sendChatMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **chat_id** | **string**|  | |
| **chat_message_input** | [**\Elev8er\PublicApi\Model\ChatMessageInput**](../Model/ChatMessageInput.md)|  | |

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
