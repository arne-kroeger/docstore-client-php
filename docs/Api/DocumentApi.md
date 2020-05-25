# OpenAPI\Client\DocumentApi

All URIs are relative to *https://documentation.perf-act.de/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addNewDocument**](DocumentApi.md#addNewDocument) | **POST** /document | adds a new document
[**addNewDocumentForTemplate**](DocumentApi.md#addNewDocumentForTemplate) | **POST** /document/template/{templateUuid} | adds a new document by template
[**getDocument**](DocumentApi.md#getDocument) | **GET** /document/{uuid}/{env} | get latest updated documents
[**getLatestDocuments**](DocumentApi.md#getLatestDocuments) | **GET** /document | get latest updated documents
[**searchDocuments**](DocumentApi.md#searchDocuments) | **POST** /document/search | search for documents



## addNewDocument

> \OpenAPI\Client\Model\Document addNewDocument($document)

adds a new document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$document = new \OpenAPI\Client\Model\Document(); // \OpenAPI\Client\Model\Document | 

try {
    $result = $apiInstance->addNewDocument($document);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->addNewDocument: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document** | [**\OpenAPI\Client\Model\Document**](../Model/Document.md)|  |

### Return type

[**\OpenAPI\Client\Model\Document**](../Model/Document.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## addNewDocumentForTemplate

> \OpenAPI\Client\Model\Document addNewDocumentForTemplate($template_uuid, $template_data)

adds a new document by template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$template_uuid = 'template_uuid_example'; // string | 
$template_data = new \OpenAPI\Client\Model\TemplateData(); // \OpenAPI\Client\Model\TemplateData | 

try {
    $result = $apiInstance->addNewDocumentForTemplate($template_uuid, $template_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->addNewDocumentForTemplate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template_uuid** | **string**|  |
 **template_data** | [**\OpenAPI\Client\Model\TemplateData**](../Model/TemplateData.md)|  |

### Return type

[**\OpenAPI\Client\Model\Document**](../Model/Document.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getDocument

> \OpenAPI\Client\Model\Document getDocument($uuid, $env)

get latest updated documents

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$uuid = 'uuid_example'; // string | 
$env = 'env_example'; // string | 

try {
    $result = $apiInstance->getDocument($uuid, $env);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->getDocument: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**|  |
 **env** | **string**|  |

### Return type

[**\OpenAPI\Client\Model\Document**](../Model/Document.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getLatestDocuments

> \OpenAPI\Client\Model\Document[] getLatestDocuments()

get latest updated documents

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getLatestDocuments();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->getLatestDocuments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\Document[]**](../Model/Document.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## searchDocuments

> \OpenAPI\Client\Model\Document[] searchDocuments($body)

search for documents

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = 'body_example'; // string | 

try {
    $result = $apiInstance->searchDocuments($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->searchDocuments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **string**|  |

### Return type

[**\OpenAPI\Client\Model\Document[]**](../Model/Document.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: text/plain
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

