# elev8er-public-api

Team-scoped public API for elev8er. Authenticate every request with an API key issued per team (`X-API-Key` header). Keys are created and managed from the elev8er panel (Team › API Keys). This API is intended for **server-to-server** use — never expose your API key in a browser or mobile client.

**Rate limiting:** every response includes `X-RateLimit-Limit`, `X-RateLimit-Remaining` and `X-RateLimit-Reset` headers. When the limit is exceeded the API returns `429 Too Many Requests`.



## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/elev8er/elev8er-php-sdk.git"
    }
  ],
  "require": {
    "elev8er/elev8er-php-sdk": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/elev8er-public-api/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AgentsApi* | [**createAgentChat**](docs/Api/AgentsApi.md#createagentchat) | **POST** /agents/{id}/chats | Start a new chat with an agent
*AgentsApi* | [**getAgent**](docs/Api/AgentsApi.md#getagent) | **GET** /agents/{id} | Get an agent by id
*AgentsApi* | [**listAgentChats**](docs/Api/AgentsApi.md#listagentchats) | **GET** /agents/{id}/chats | List chats for an agent
*AgentsApi* | [**listAgents**](docs/Api/AgentsApi.md#listagents) | **GET** /agents | List agents
*AgentsApi* | [**listChatMessages**](docs/Api/AgentsApi.md#listchatmessages) | **GET** /agents/{id}/chats/{chatId}/messages | Get messages in a chat
*AgentsApi* | [**sendChatMessage**](docs/Api/AgentsApi.md#sendchatmessage) | **POST** /agents/{id}/chats/{chatId}/messages | Send a message to the agent and get its reply (non-streaming)
*BlogsApi* | [**createBlog**](docs/Api/BlogsApi.md#createblog) | **POST** /blogs | Create a blog
*BlogsApi* | [**deleteBlog**](docs/Api/BlogsApi.md#deleteblog) | **DELETE** /blogs/{id} | Delete a blog
*BlogsApi* | [**getBlog**](docs/Api/BlogsApi.md#getblog) | **GET** /blogs/{id} | Get a blog by id
*BlogsApi* | [**listBlogs**](docs/Api/BlogsApi.md#listblogs) | **GET** /blogs | List blogs
*BlogsApi* | [**updateBlog**](docs/Api/BlogsApi.md#updateblog) | **PUT** /blogs/{id} | Update a blog
*ExpertsApi* | [**createAvailability**](docs/Api/ExpertsApi.md#createavailability) | **POST** /experts/availability | Create an availability entry
*ExpertsApi* | [**createExpert**](docs/Api/ExpertsApi.md#createexpert) | **POST** /experts | Create an expert
*ExpertsApi* | [**createSession**](docs/Api/ExpertsApi.md#createsession) | **POST** /experts/sessions | Create a session
*ExpertsApi* | [**deleteAvailability**](docs/Api/ExpertsApi.md#deleteavailability) | **DELETE** /experts/availability/{id} | Delete an availability entry
*ExpertsApi* | [**deleteExpert**](docs/Api/ExpertsApi.md#deleteexpert) | **DELETE** /experts/{id} | Delete an expert
*ExpertsApi* | [**deleteSession**](docs/Api/ExpertsApi.md#deletesession) | **DELETE** /experts/sessions/{id} | Delete a session
*ExpertsApi* | [**getAvailability**](docs/Api/ExpertsApi.md#getavailability) | **GET** /experts/availability/{id} | Get an availability entry
*ExpertsApi* | [**getExpert**](docs/Api/ExpertsApi.md#getexpert) | **GET** /experts/{id} | Get an expert by id
*ExpertsApi* | [**getExpertAvailability**](docs/Api/ExpertsApi.md#getexpertavailability) | **GET** /experts/{expertId}/availability | Get an expert&#39;s availability
*ExpertsApi* | [**getSession**](docs/Api/ExpertsApi.md#getsession) | **GET** /experts/sessions/{id} | Get a session
*ExpertsApi* | [**listExpertSessions**](docs/Api/ExpertsApi.md#listexpertsessions) | **GET** /experts/{expertId}/sessions | List sessions for an expert
*ExpertsApi* | [**listExperts**](docs/Api/ExpertsApi.md#listexperts) | **GET** /experts | List experts
*ExpertsApi* | [**listSessions**](docs/Api/ExpertsApi.md#listsessions) | **GET** /experts/sessions | List sessions
*ExpertsApi* | [**setExpertAvailability**](docs/Api/ExpertsApi.md#setexpertavailability) | **PUT** /experts/{expertId}/availability | Replace an expert&#39;s availability
*ExpertsApi* | [**updateAvailability**](docs/Api/ExpertsApi.md#updateavailability) | **PUT** /experts/availability/{id} | Update an availability entry
*ExpertsApi* | [**updateExpert**](docs/Api/ExpertsApi.md#updateexpert) | **PUT** /experts/{id} | Update an expert
*ExpertsApi* | [**updateSession**](docs/Api/ExpertsApi.md#updatesession) | **PUT** /experts/sessions/{id} | Update a session
*ExpertsApi* | [**updateSessionStatus**](docs/Api/ExpertsApi.md#updatesessionstatus) | **PATCH** /experts/sessions/{id}/status | Update a session&#39;s status
*ProgramsApi* | [**createProgram**](docs/Api/ProgramsApi.md#createprogram) | **POST** /programs | Create a program
*ProgramsApi* | [**createProgramTag**](docs/Api/ProgramsApi.md#createprogramtag) | **POST** /programs/tags | Create a program tag
*ProgramsApi* | [**createProgramVersion**](docs/Api/ProgramsApi.md#createprogramversion) | **POST** /programs/{id}/versions | Create a new version of a program
*ProgramsApi* | [**deleteProgram**](docs/Api/ProgramsApi.md#deleteprogram) | **DELETE** /programs/{id} | Delete a program
*ProgramsApi* | [**deleteProgramTag**](docs/Api/ProgramsApi.md#deleteprogramtag) | **DELETE** /programs/tags/{tagId} | Delete a program tag
*ProgramsApi* | [**getProgram**](docs/Api/ProgramsApi.md#getprogram) | **GET** /programs/{id} | Get a program by id
*ProgramsApi* | [**getProgramTags**](docs/Api/ProgramsApi.md#getprogramtags) | **GET** /programs/{id}/tags | Get tags assigned to a program
*ProgramsApi* | [**getProgramVersion**](docs/Api/ProgramsApi.md#getprogramversion) | **GET** /programs/{id}/versions/{versionId} | Get a specific program version
*ProgramsApi* | [**listProgramTags**](docs/Api/ProgramsApi.md#listprogramtags) | **GET** /programs/tags | List program tags
*ProgramsApi* | [**listProgramVersions**](docs/Api/ProgramsApi.md#listprogramversions) | **GET** /programs/{id}/versions | List versions of a program
*ProgramsApi* | [**listPrograms**](docs/Api/ProgramsApi.md#listprograms) | **GET** /programs | List programs
*ProgramsApi* | [**rollbackProgramVersion**](docs/Api/ProgramsApi.md#rollbackprogramversion) | **POST** /programs/{id}/versions/{versionId}/rollback | Roll a program back to a specific version
*ProgramsApi* | [**setProgramTags**](docs/Api/ProgramsApi.md#setprogramtags) | **PUT** /programs/{id}/tags | Replace the tags assigned to a program
*ProgramsApi* | [**updateProgram**](docs/Api/ProgramsApi.md#updateprogram) | **PUT** /programs/{id} | Update a program
*ProgramsApi* | [**updateProgramTag**](docs/Api/ProgramsApi.md#updateprogramtag) | **PUT** /programs/tags/{tagId} | Update a program tag
*ProgramsApi* | [**updateProgramVersion**](docs/Api/ProgramsApi.md#updateprogramversion) | **PUT** /programs/{id}/versions/{versionId} | Update a specific program version
*TestsApi* | [**createTest**](docs/Api/TestsApi.md#createtest) | **POST** /tests | Create a test
*TestsApi* | [**createTestVersion**](docs/Api/TestsApi.md#createtestversion) | **POST** /tests/{id}/versions | Create a new version of a test
*TestsApi* | [**deleteTest**](docs/Api/TestsApi.md#deletetest) | **DELETE** /tests/{id} | Delete a test
*TestsApi* | [**getTest**](docs/Api/TestsApi.md#gettest) | **GET** /tests/{id} | Get a test by id
*TestsApi* | [**getTestVersion**](docs/Api/TestsApi.md#gettestversion) | **GET** /tests/{id}/versions/{versionId} | Get a specific test version
*TestsApi* | [**listTestVersions**](docs/Api/TestsApi.md#listtestversions) | **GET** /tests/{id}/versions | List versions of a test
*TestsApi* | [**listTests**](docs/Api/TestsApi.md#listtests) | **GET** /tests | List tests
*TestsApi* | [**rollbackTestVersion**](docs/Api/TestsApi.md#rollbacktestversion) | **POST** /tests/{id}/versions/{versionId}/rollback | Roll a test back to a specific version
*TestsApi* | [**updateTest**](docs/Api/TestsApi.md#updatetest) | **PUT** /tests/{id} | Update a test
*TestsApi* | [**updateTestVersion**](docs/Api/TestsApi.md#updatetestversion) | **PUT** /tests/{id}/versions/{versionId} | Update a specific test version
*VisualTestsApi* | [**createVisualTest**](docs/Api/VisualTestsApi.md#createvisualtest) | **POST** /visual-tests | Create a visual test
*VisualTestsApi* | [**createVisualTestVersion**](docs/Api/VisualTestsApi.md#createvisualtestversion) | **POST** /visual-tests/{id}/versions | Create a new version of a visual test
*VisualTestsApi* | [**deleteVisualTest**](docs/Api/VisualTestsApi.md#deletevisualtest) | **DELETE** /visual-tests/{id} | Delete a visual test
*VisualTestsApi* | [**getVisualTest**](docs/Api/VisualTestsApi.md#getvisualtest) | **GET** /visual-tests/{id} | Get a visual test by id
*VisualTestsApi* | [**getVisualTestVersion**](docs/Api/VisualTestsApi.md#getvisualtestversion) | **GET** /visual-tests/{id}/versions/{versionId} | Get a specific visual test version
*VisualTestsApi* | [**listVisualTestVersions**](docs/Api/VisualTestsApi.md#listvisualtestversions) | **GET** /visual-tests/{id}/versions | List versions of a visual test
*VisualTestsApi* | [**listVisualTests**](docs/Api/VisualTestsApi.md#listvisualtests) | **GET** /visual-tests | List visual tests
*VisualTestsApi* | [**rollbackVisualTestVersion**](docs/Api/VisualTestsApi.md#rollbackvisualtestversion) | **POST** /visual-tests/{id}/versions/{versionId}/rollback | Roll a visual test back to a specific version
*VisualTestsApi* | [**updateVisualTest**](docs/Api/VisualTestsApi.md#updatevisualtest) | **PUT** /visual-tests/{id} | Update a visual test
*VisualTestsApi* | [**updateVisualTestVersion**](docs/Api/VisualTestsApi.md#updatevisualtestversion) | **PUT** /visual-tests/{id}/versions/{versionId} | Update a specific visual test version

## Models

- [ChatMessageInput](docs/Model/ChatMessageInput.md)
- [CreateAgentChatRequest](docs/Model/CreateAgentChatRequest.md)
- [CreateProgramTagRequest](docs/Model/CreateProgramTagRequest.md)
- [Error](docs/Model/Error.md)
- [ListPrograms200Response](docs/Model/ListPrograms200Response.md)
- [Pagination](docs/Model/Pagination.md)
- [SetProgramTagsRequest](docs/Model/SetProgramTagsRequest.md)
- [SuccessEnvelope](docs/Model/SuccessEnvelope.md)
- [UpdateProgramTagRequest](docs/Model/UpdateProgramTagRequest.md)
- [UpdateSessionStatusRequest](docs/Model/UpdateSessionStatusRequest.md)

## Authorization

Authentication schemes defined for the API:
### ApiKeyAuth

- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

support@elev8er.ai

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
    - Package version: `1.0.0`
    - Generator version: `7.7.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
