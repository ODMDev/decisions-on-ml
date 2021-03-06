# openapi-java-client

API
- API version: 1.0
  - Build date: 2020-04-04T21:42:30.084329+02:00[Europe/Paris]

No description provided (generated by Openapi Generator https://github.com/openapitools/openapi-generator)


*Automatically generated by the [OpenAPI Generator](https://openapi-generator.tech)*


## Requirements

Building the API client library requires:
1. Java 1.7+
2. Maven/Gradle

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>org.openapitools</groupId>
  <artifactId>openapi-java-client</artifactId>
  <version>1.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "org.openapitools:openapi-java-client:1.0"
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/openapi-java-client-1.0.jar`
* `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.AutomationApiV10PredictionAdminApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AutomationApiV10PredictionAdminApi apiInstance = new AutomationApiV10PredictionAdminApi(defaultClient);
    try {
      apiInstance.getHeartBeat();
    } catch (ApiException e) {
      System.err.println("Exception when calling AutomationApiV10PredictionAdminApi#getHeartBeat");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}

```

## Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AutomationApiV10PredictionAdminApi* | [**getHeartBeat**](docs/AutomationApiV10PredictionAdminApi.md#getHeartBeat) | **GET** /automation/api/v1.0/prediction/admin/isAlive | 
*AutomationApiV10PredictionAdminApi* | [**getModel**](docs/AutomationApiV10PredictionAdminApi.md#getModel) | **GET** /automation/api/v1.0/prediction/admin/models | Returns the list of ML models
*AutomationApiV10PredictionAdminApi* | [**postModelSchema**](docs/AutomationApiV10PredictionAdminApi.md#postModelSchema) | **POST** /automation/api/v1.0/prediction/admin/ModelSchema | Returns the schema of a model
*AutomationApiV10PredictionGenericApi* | [**postPredictionService**](docs/AutomationApiV10PredictionGenericApi.md#postPredictionService) | **POST** /automation/api/v1.0/prediction/generic/ | Computes a new prediction


## Documentation for Models

 - [ModelDescriptor](docs/ModelDescriptor.md)
 - [ModelKetDescriptor](docs/ModelKetDescriptor.md)
 - [ModelMetadata](docs/ModelMetadata.md)
 - [ModelSchema](docs/ModelSchema.md)
 - [PredictionRequest](docs/PredictionRequest.md)
 - [PredictionResponse](docs/PredictionResponse.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author



