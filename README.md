# OpenAPIClient-php

Connect your software to POEditor with this simple API


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
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');




$apiInstance = new OpenAPI\Client\Api\ContributorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$api_token = 'api_token_example'; // string
$id = 'id_example'; // string | The id of project
$name = 'name_example'; // string | The name of contributor
$email = 'email_example'; // string | The email of contributor
$language = 'language_example'; // string | The language code (Required if adding a contributor)
$admin = 56; // int | Set it to 1 for adding as administrator

try {
    $result = $apiInstance->contributorsAddPost($api_token, $id, $name, $email, $language, $admin);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContributorsApi->contributorsAddPost: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.poeditor.com/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ContributorsApi* | [**contributorsAddPost**](docs/Api/ContributorsApi.md#contributorsaddpost) | **POST** /contributors/add | Adds a contributor to a project language or an administrator to a project.
*ContributorsApi* | [**contributorsListPost**](docs/Api/ContributorsApi.md#contributorslistpost) | **POST** /contributors/list | Returns the list of contributors from your projects.
*ContributorsApi* | [**contributorsRemovePost**](docs/Api/ContributorsApi.md#contributorsremovepost) | **POST** /contributors/remove | Removes a contributor from a project language or an admin from a project, if the language is not specified.
*LanguagesApi* | [**languagesAddPost**](docs/Api/LanguagesApi.md#languagesaddpost) | **POST** /languages/add | Adds a new language to project.
*LanguagesApi* | [**languagesAvailablePost**](docs/Api/LanguagesApi.md#languagesavailablepost) | **POST** /languages/available | Returns project languages, percentage of translation done for each and the datetime (UTC - ISO 8601) when the last change was made.
*LanguagesApi* | [**languagesDeletePost**](docs/Api/LanguagesApi.md#languagesdeletepost) | **POST** /languages/delete | Deletes existing language from project.
*LanguagesApi* | [**languagesListPost**](docs/Api/LanguagesApi.md#languageslistpost) | **POST** /languages/list | Returns project languages, percentage of translation done for each and the datetime (UTC - ISO 8601) when the last change was made.
*LanguagesApi* | [**languagesUpdatePost**](docs/Api/LanguagesApi.md#languagesupdatepost) | **POST** /languages/update | Inserts / overwrites translations.
*ProjectsApi* | [**projectsAddPost**](docs/Api/ProjectsApi.md#projectsaddpost) | **POST** /projects/add | Creates a new project. Returns project details (if successful)
*ProjectsApi* | [**projectsDeletePost**](docs/Api/ProjectsApi.md#projectsdeletepost) | **POST** /projects/delete | Deletes the project from the account. You must be the owner of the project.
*ProjectsApi* | [**projectsExportPost**](docs/Api/ProjectsApi.md#projectsexportpost) | **POST** /projects/export | Returns the link of the file (expires after 10 minutes). The settings inherited from the project will be the ones at the time of the download.
*ProjectsApi* | [**projectsListPost**](docs/Api/ProjectsApi.md#projectslistpost) | **POST** /projects/list | Returns the list of projects owned by user.
*ProjectsApi* | [**projectsSyncPost**](docs/Api/ProjectsApi.md#projectssyncpost) | **POST** /projects/sync | Syncs your project with the array you send (terms that are not found in the JSON object will be deleted from project and the new ones added). Please use with caution. If wrong data is sent, existing terms and their translations might be irreversibly lost.
*ProjectsApi* | [**projectsUpdatePost**](docs/Api/ProjectsApi.md#projectsupdatepost) | **POST** /projects/update | Updates project settings (name, description, reference language, fallback language). If optional parameters are not sent, their respective fields are not updated.
*ProjectsApi* | [**projectsUploadPost**](docs/Api/ProjectsApi.md#projectsuploadpost) | **POST** /projects/upload | Updates terms / translations - No more than one request every 30 seconds.
*ProjectsApi* | [**projectsViewPost**](docs/Api/ProjectsApi.md#projectsviewpost) | **POST** /projects/view | Returns projects details
*TermsApi* | [**termsAddCommentPost**](docs/Api/TermsApi.md#termsaddcommentpost) | **POST** /terms/add_comment | Adds comments to existing terms.
*TermsApi* | [**termsAddPost**](docs/Api/TermsApi.md#termsaddpost) | **POST** /terms/add | Adds terms to project.
*TermsApi* | [**termsDeletePost**](docs/Api/TermsApi.md#termsdeletepost) | **POST** /terms/delete | Deletes terms from project.
*TermsApi* | [**termsListPost**](docs/Api/TermsApi.md#termslistpost) | **POST** /terms/list | Returns project&#39;s terms and translations if the argument language is provided.
*TermsApi* | [**termsUpdatePost**](docs/Api/TermsApi.md#termsupdatepost) | **POST** /terms/update | Updates project terms. Lets you change the text, context, reference, plural and tags.
*TranslationsApi* | [**translationsAddPost**](docs/Api/TranslationsApi.md#translationsaddpost) | **POST** /translations/add | Adds translations to project. If translation exists, it will not overwrite it.
*TranslationsApi* | [**translationsDeletePost**](docs/Api/TranslationsApi.md#translationsdeletepost) | **POST** /translations/delete | Deletes translations from specified language.
*TranslationsApi* | [**translationsUpdatePost**](docs/Api/TranslationsApi.md#translationsupdatepost) | **POST** /translations/update | Updates existing translations.

## Models

- [ContributorsListResponse](docs/Model/ContributorsListResponse.md)
- [ContributorsListResponseAllOf](docs/Model/ContributorsListResponseAllOf.md)
- [ContributorsListResponseAllOfResult](docs/Model/ContributorsListResponseAllOfResult.md)
- [ContributorsListResponseAllOfResultContributors](docs/Model/ContributorsListResponseAllOfResultContributors.md)
- [ContributorsListResponseAllOfResultPermissions](docs/Model/ContributorsListResponseAllOfResultPermissions.md)
- [ContributorsListResponseAllOfResultProject](docs/Model/ContributorsListResponseAllOfResultProject.md)
- [LanguagesListLong](docs/Model/LanguagesListLong.md)
- [LanguagesListLongLanguagesInner](docs/Model/LanguagesListLongLanguagesInner.md)
- [LanguagesListLongResponse](docs/Model/LanguagesListLongResponse.md)
- [LanguagesListLongResponseAllOf](docs/Model/LanguagesListLongResponseAllOf.md)
- [LanguagesListShort](docs/Model/LanguagesListShort.md)
- [LanguagesListShortLanguagesInner](docs/Model/LanguagesListShortLanguagesInner.md)
- [LanguagesListShortResponse](docs/Model/LanguagesListShortResponse.md)
- [LanguagesListShortResponseAllOf](docs/Model/LanguagesListShortResponseAllOf.md)
- [ProjectExportResponse](docs/Model/ProjectExportResponse.md)
- [ProjectExportResponseAllOf](docs/Model/ProjectExportResponseAllOf.md)
- [ProjectExportResponseAllOfResult](docs/Model/ProjectExportResponseAllOfResult.md)
- [ProjectList](docs/Model/ProjectList.md)
- [ProjectListProjectsInner](docs/Model/ProjectListProjectsInner.md)
- [ProjectListResponse](docs/Model/ProjectListResponse.md)
- [ProjectListResponseAllOf](docs/Model/ProjectListResponseAllOf.md)
- [ProjectLong](docs/Model/ProjectLong.md)
- [ProjectLongProject](docs/Model/ProjectLongProject.md)
- [ProjectSyncResponse](docs/Model/ProjectSyncResponse.md)
- [ProjectSyncResponseAllOf](docs/Model/ProjectSyncResponseAllOf.md)
- [ProjectUploadResponse](docs/Model/ProjectUploadResponse.md)
- [ProjectUploadResponseAllOf](docs/Model/ProjectUploadResponseAllOf.md)
- [ProjectViewResponse](docs/Model/ProjectViewResponse.md)
- [ProjectViewResponseAllOf](docs/Model/ProjectViewResponseAllOf.md)
- [Response](docs/Model/Response.md)
- [ResponseResponse](docs/Model/ResponseResponse.md)
- [TermAddCommentResponse](docs/Model/TermAddCommentResponse.md)
- [TermAddCommentResponseAllOf](docs/Model/TermAddCommentResponseAllOf.md)
- [TermAddedResponse](docs/Model/TermAddedResponse.md)
- [TermAddedResponseAllOf](docs/Model/TermAddedResponseAllOf.md)
- [TermDeletedResponse](docs/Model/TermDeletedResponse.md)
- [TermDeletedResponseAllOf](docs/Model/TermDeletedResponseAllOf.md)
- [TermUpdatedResponse](docs/Model/TermUpdatedResponse.md)
- [TermUpdatedResponseAllOf](docs/Model/TermUpdatedResponseAllOf.md)
- [TermsFull](docs/Model/TermsFull.md)
- [TermsFullTerms](docs/Model/TermsFullTerms.md)
- [TermsListFull](docs/Model/TermsListFull.md)
- [TermsListFullResponse](docs/Model/TermsListFullResponse.md)
- [TermsListFullResponseAllOf](docs/Model/TermsListFullResponseAllOf.md)
- [TermsListFullTermsInner](docs/Model/TermsListFullTermsInner.md)
- [TermsListFullTermsInnerTranslation](docs/Model/TermsListFullTermsInnerTranslation.md)
- [TermsLong](docs/Model/TermsLong.md)
- [TermsLongTerms](docs/Model/TermsLongTerms.md)
- [TermsShortAdded](docs/Model/TermsShortAdded.md)
- [TermsShortAddedTerms](docs/Model/TermsShortAddedTerms.md)
- [TermsShortComment](docs/Model/TermsShortComment.md)
- [TermsShortCommentTerms](docs/Model/TermsShortCommentTerms.md)
- [TermsShortDeleted](docs/Model/TermsShortDeleted.md)
- [TermsShortDeletedTerms](docs/Model/TermsShortDeletedTerms.md)
- [TermsShortUpdated](docs/Model/TermsShortUpdated.md)
- [TermsShortUpdatedTerms](docs/Model/TermsShortUpdatedTerms.md)
- [TermsTranslationsResponse](docs/Model/TermsTranslationsResponse.md)
- [TranslationAddedResponse](docs/Model/TranslationAddedResponse.md)
- [TranslationAddedResponseAllOf](docs/Model/TranslationAddedResponseAllOf.md)
- [TranslationDeletedResponse](docs/Model/TranslationDeletedResponse.md)
- [TranslationDeletedResponseAllOf](docs/Model/TranslationDeletedResponseAllOf.md)
- [TranslationUpdatedResponse](docs/Model/TranslationUpdatedResponse.md)
- [TranslationUpdatedResponseAllOf](docs/Model/TranslationUpdatedResponseAllOf.md)
- [TranslationsLong](docs/Model/TranslationsLong.md)
- [TranslationsShort](docs/Model/TranslationsShort.md)
- [TranslationsShortAdded](docs/Model/TranslationsShortAdded.md)
- [TranslationsShortDeleted](docs/Model/TranslationsShortDeleted.md)
- [TranslationsShortResponse](docs/Model/TranslationsShortResponse.md)
- [TranslationsShortResponseAllOf](docs/Model/TranslationsShortResponseAllOf.md)
- [TranslationsShortTranslations](docs/Model/TranslationsShortTranslations.md)
- [TranslationsShortUpdated](docs/Model/TranslationsShortUpdated.md)

## Authorization
All endpoints do not require authorization.
## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.3`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
