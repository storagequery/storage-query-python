# storagequery.StorageQuerySQLApi

All URIs are relative to *https://api.storagequery.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**run_sql_query**](StorageQuerySQLApi.md#run_sql_query) | **POST** /data_access/sql | 


# **run_sql_query**
> SuccessResponseDataAccessSql run_sql_query(authorization, content_type, request_body_data_access_sql=request_body_data_access_sql)



Execute SQL queries over StorageQuery data connections.

### Example

* Api Key Authentication (ApiKeyAuth):
```python
from __future__ import print_function
import time
import storagequery
from storagequery.rest import ApiException
from pprint import pprint
configuration = storagequery.Configuration()
# Configure API key authorization: ApiKeyAuth
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# Defining host is optional and default to https://api.storagequery.com/v1
configuration.host = "https://api.storagequery.com/v1"

# Enter a context with an instance of the API client
with storagequery.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = storagequery.StorageQuerySQLApi(api_client)
    authorization = 'authorization_example' # str | Defines the user authorization API key
content_type = 'content_type_example' # str | Defines the request content media type
request_body_data_access_sql = storagequery.RequestBodyDataAccessSql() # RequestBodyDataAccessSql |  (optional)

    try:
        api_response = api_instance.run_sql_query(authorization, content_type, request_body_data_access_sql=request_body_data_access_sql)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling StorageQuerySQLApi->run_sql_query: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**| Defines the user authorization API key | 
 **content_type** | **str**| Defines the request content media type | 
 **request_body_data_access_sql** | [**RequestBodyDataAccessSql**](RequestBodyDataAccessSql.md)|  | [optional] 

### Return type

[**SuccessResponseDataAccessSql**](SuccessResponseDataAccessSql.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request was completed successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

