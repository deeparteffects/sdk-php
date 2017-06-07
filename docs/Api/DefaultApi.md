# Deeparteffects\Client\DefaultApi

All URIs are relative to *https://api.deeparteffects.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**resultGet**](DefaultApi.md#resultGet) | **GET** /result | 
[**stylesGet**](DefaultApi.md#stylesGet) | **GET** /styles | 
[**uploadPost**](DefaultApi.md#uploadPost) | **POST** /upload | 


# **resultGet**
> \Deeparteffects\Client\Model\Result resultGet($submission_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_key = '--Your API Key--';
$access_key = '--Your ACCESS Key--';
$secret_key = '--Your SECRET KEY--';

$api_instance = new \Deeparteffects\Client\Api\DefaultApi();
$api_instance->setApiKey($api_key);
$api_instance->setApiAccessKey($access_key);
$api_instance->setApiSecretKey($secret_key);

$submission_id = "submission_id_example"; // string | 

try {
    $result = $api_instance->resultGet($submission_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->resultGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **submission_id** | **string**|  | [optional]

### Return type

[**\Deeparteffects\Client\Model\Result**](../Model/Result.md)

### Authorization

[api_key](../../README.md#api_key), [sigv4](../../README.md#sigv4)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


# **stylesGet**
> \Deeparteffects\Client\Model\Styles stylesGet()


### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_key = '--Your API Key--';
$access_key = '--Your ACCESS Key--';
$secret_key = '--Your SECRET KEY--';

$api_instance = new \Deeparteffects\Client\Api\DefaultApi();
$api_instance->setApiKey($api_key);
$api_instance->setApiAccessKey($access_key);
$api_instance->setApiSecretKey($secret_key);

try {
    $result = $api_instance->stylesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->stylesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Deeparteffects\Client\Model\Styles**](../Model/Styles.md)

### Authorization

[api_key](../../README.md#api_key), [sigv4](../../README.md#sigv4)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


# **uploadPost**
> \Deeparteffects\Client\Model\UploadResponse uploadPost($upload_request)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_key = '--Your API Key--';
$access_key = '--Your ACCESS Key--';
$secret_key = '--Your SECRET KEY--';

$api_instance = new \Deeparteffects\Client\Api\DefaultApi();
$api_instance->setApiKey($api_key);
$api_instance->setApiAccessKey($access_key);
$api_instance->setApiSecretKey($secret_key);

$upload_request = new \Deeparteffects\Client\Model\UploadRequest(); // \Deeparteffects\Client\Model\UploadRequest | 

try {
    $image = base64_encode(file_get_contents("/path/to/image"));
    $uploadRequest->setStyleId("Unique style id");
    $uploadRequest->setImageBase64Encoded($image);
    $result = $api_instance->uploadPost($upload_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->uploadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **upload_request** | [**\Deeparteffects\Client\Model\UploadRequest**](../Model/\Deeparteffects\Client\Model\UploadRequest.md)|  |

### Return type

[**\Deeparteffects\Client\Model\UploadResponse**](../Model/UploadResponse.md)

### Authorization

[api_key](../../README.md#api_key), [sigv4](../../README.md#sigv4)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

