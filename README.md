# ![LOGO](logo.png) Cloud Search **flow**ground Connector

## Description

A generated **flow**ground connector for the Cloud Search API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/cloudsearch/v1/swagger.json<br/>
Generated at: 2019-05-07T17:41:20+03:00

## API Description

Cloud Search provides cloud-based search capabilities over G Suite data.  The Cloud Search API allows indexing of non-G Suite data into Cloud Search.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Fetches the item whose viewUrl exactly matches that of the URL provided<br/>
> in the request.

*Tags:* `debug`

#### Input Parameters
* `name` - _required_ - Source name, format:
datasources/{source_id}
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Checks whether an item is accessible by specified principal.

*Tags:* `debug`

#### Input Parameters
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `name` - _required_ - Item name, format:
datasources/{source_id}/items/{item_id}
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists names of items associated with an unmapped identity.

*Tags:* `debug`

#### Input Parameters
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `groupResourceName` - _optional_
* `pageSize` - _optional_ - Maximum number of items to fetch in a request.
Defaults to 100.
* `pageToken` - _optional_ - The next_page_token value returned from a previous List request, if any.
* `parent` - _required_ - The name of the identity source, in the following format:
identitysources/{source_id}}
* `userResourceName` - _optional_
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists unmapped user identities for an identity source.

*Tags:* `debug`

#### Input Parameters
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `pageSize` - _optional_ - Maximum number of items to fetch in a request.
Defaults to 100.
* `pageToken` - _optional_ - The next_page_token value returned from a previous List request, if any.
* `parent` - _required_ - The name of the identity source, in the following format:
identitysources/{source_id}
* `resolutionStatusCode` - _optional_ - Limit users selection to this status.
    Possible values: CODE_UNSPECIFIED, NOT_FOUND, IDENTITY_SOURCE_NOT_FOUND, IDENTITY_SOURCE_MISCONFIGURED, TOO_MANY_MAPPINGS_FOUND, INTERNAL_ERROR.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes Item resource for the<br/>
> specified resource name.

*Tags:* `indexing`

#### Input Parameters
* `connectorName` - _optional_ - Name of connector making this call.
<br />Format: datasources/{source_id}/connectors/{ID}
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `mode` - _optional_ - Required. The RequestMode for this request.
    Possible values: UNSPECIFIED, SYNCHRONOUS, ASYNCHRONOUS.
* `name` - _required_ - Required. Name of the item to delete.
Format: datasources/{source_id}/items/{item_id}
* `version` - _optional_ - Required. The incremented version of the item to delete from the index.
The indexing system stores the version from the datasource as a
byte string and compares the Item version in the index
to the version of the queued Item using lexical ordering.
<br /><br />
Cloud Search Indexing won't delete any queued item with
a version value that is less than or equal to
the version of the currently indexed item.
The maximum length for this field is 1024 bytes.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets Item resource by item name.

*Tags:* `indexing`

#### Input Parameters
* `connectorName` - _optional_ - Name of connector making this call.
<br />Format: datasources/{source_id}/connectors/{ID}
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `name` - _required_ - Name of the item to get info.
Format: datasources/{source_id}/items/{item_id}
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists all or a subset of Item resources.

*Tags:* `indexing`

#### Input Parameters
* `brief` - _optional_ - When set to true, the indexing system only populates the following fields:
name,
version,
metadata.hash,
structured_data.hash,
content.hash.
<br />If this value is false, then all the fields are populated in Item.
* `connectorName` - _optional_ - Name of connector making this call.
<br />Format: datasources/{source_id}/connectors/{ID}
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `name` - _required_ - Name of the Data Source to list Items.  Format:
datasources/{source_id}
* `pageSize` - _optional_ - Maximum number of items to fetch in a request.
The max value is 1000 when brief is true.  The max value is 10 if brief
is false.
<br />The default value is 10
* `pageToken` - _optional_ - The next_page_token value returned from a previous List request, if any.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes all items in a queue. This method is useful for deleting stale<br/>
> items.

*Tags:* `indexing`

#### Input Parameters
* `name` - _required_ - Name of the Data Source to delete items in a queue.
Format: datasources/{source_id}
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Polls for unreserved items from the indexing queue and marks a<br/>
> set as reserved, starting with items that have<br/>
> the oldest timestamp from the highest priority<br/>
> ItemStatus.<br/>
> The priority order is as follows: <br /><br/>
> ERROR<br/>
> <br /><br/>
> MODIFIED<br/>
> <br /><br/>
> NEW_ITEM<br/>
> <br /><br/>
> ACCEPTED<br/>
> <br /><br/>
> Reserving items ensures that polling from other threads<br/>
> cannot create overlapping sets.<br/>
> <br/>
> After handling the reserved items, the client should put items back<br/>
> into the unreserved state, either by calling<br/>
> index,<br/>
> or by calling<br/>
> push with<br/>
> the type REQUEUE.<br/>
> <br/>
> Items automatically become available (unreserved) after 4 hours even if no<br/>
> update or push method is called.

*Tags:* `indexing`

#### Input Parameters
* `name` - _required_ - Name of the Data Source to poll items.
Format: datasources/{source_id}
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Unreserves all items from a queue, making them all eligible to be<br/>
> polled.  This method is useful for resetting the indexing queue<br/>
> after a connector has been restarted.

*Tags:* `indexing`

#### Input Parameters
* `name` - _required_ - Name of the Data Source to unreserve all items.
Format: datasources/{source_id}
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes the schema of a data source.

*Tags:* `indexing`

#### Input Parameters
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `name` - _required_ - Name of the data source to delete Schema.  Format:
datasources/{source_id}
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the schema of a data source.

*Tags:* `indexing`

#### Input Parameters
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `name` - _required_ - Name of the data source to get Schema.  Format:
datasources/{source_id}
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates the schema of a data source.

*Tags:* `indexing`

#### Input Parameters
* `name` - _required_ - Name of the data source to update Schema.  Format:
datasources/{source_id}
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates Item ACL, metadata, and<br/>
> content. It will insert the Item if it<br/>
> does not exist.<br/>
> This method does not support partial updates.  Fields with no provided<br/>
> values are cleared out in the Cloud Search index.

*Tags:* `indexing`

#### Input Parameters
* `name` - _required_ - Name of the Item. Format:
datasources/{source_id}/items/{item_id}
<br />This is a required field.
The maximum length is 1536 characters.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Pushes an item onto a queue for later polling and updating.

*Tags:* `indexing`

#### Input Parameters
* `name` - _required_ - Name of the item to
push into the indexing queue.<br />
Format: datasources/{source_id}/items/{ID}
<br />This is a required field.
The maximum length is 1536 characters.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates an upload session for uploading item content. For items smaller<br/>
> than 100 KiB, it's easier to embed the content<br/>
> inline within<br/>
> update.

*Tags:* `indexing`

#### Input Parameters
* `name` - _required_ - Name of the Data Source to start a resumable upload.
Format: datasources/{source_id}
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Uploads media for indexing.<br/>
> <br/>
> The upload endpoint supports direct and resumable upload protocols and<br/>
> is intended for large items that can not be inlined during index requests. To<br/>
> index large content:<br/>
> <br/>
> 1. Call upload to begin<br/>
>    a session and get the item reference.<br/>
> 1. Upload the content using the item reference's resource name.<br/>
> 1. Call index with the item<br/>
>    reference as the content.<br/>
> <br/>
> For additional information, see<br/>
> [Create a content connector using the REST API](https://developers.google.com/cloud-search/docs/guides/content-connector#rest).

*Tags:* `media`

#### Input Parameters
* `resourceName` - _required_ - Name of the media that is being downloaded.  See
ReadRequest.resource_name.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### The Cloud Search Query API provides the search method, which returns<br/>
> the most relevant results from a user query.  The results can come from<br/>
> G Suite Apps, such as Gmail or Google Drive, or they can come from data<br/>
> that you have indexed from a third party.

*Tags:* `query`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns list of sources that user can use for Search and Suggest APIs.

*Tags:* `query`

#### Input Parameters
* `pageToken` - _optional_ - Number of sources to return in the response.
* `requestOptions.debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `requestOptions.languageCode` - _optional_ - The BCP-47 language code, such as "en-US" or "sr-Latn".
For more information, see
http://www.unicode.org/reports/tr35/#Unicode_locale_identifier.
For translations.
* `requestOptions.searchApplicationId` - _optional_ - Id of the application created using SearchApplicationsService.
* `requestOptions.timeZone` - _optional_ - Current user's time zone id, such as "America/Los_Angeles" or
"Australia/Sydney". These IDs are defined by
[Unicode Common Locale Data Repository (CLDR)](http://cldr.unicode.org/)
project, and currently available in the file
[timezone.xml](http://unicode.org/repos/cldr/trunk/common/bcp47/timezone.xml)
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Provides suggestions for autocompleting the query.

*Tags:* `query`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists datasources.

*Tags:* `settings`

#### Input Parameters
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `pageSize` - _optional_ - Maximum number of datasources to fetch in a request.
The max value is 100.
<br />The default value is 10
* `pageToken` - _optional_ - Starting index of the results.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a datasource.

*Tags:* `settings`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists all search applications.

*Tags:* `settings`

#### Input Parameters
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `pageSize` - _optional_ - The maximum number of items to return.
* `pageToken` - _optional_ - The next_page_token value returned from a previous List request, if any.
<br/> The default value is 10
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a search application.

*Tags:* `settings`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes a search application.

*Tags:* `settings`

#### Input Parameters
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `name` - _required_ - The name of the search application to be deleted.
<br />Format: applications/{application_id}.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the specified search application.

*Tags:* `settings`

#### Input Parameters
* `debugOptions.enableDebugging` - _optional_ - If set, the request will enable debugging features of Cloud Search.
Only turn on this field, if asked by Google to help with debugging.
* `name` - _required_ - Name of the search application.
<br />Format: applications/{application_id}.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates a search application.

*Tags:* `settings`

#### Input Parameters
* `name` - _required_ - Name of the Search Application.
<br />Format: searchapplications/{application_id}.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Resets a search application to default settings. This will return an empty<br/>
> response.

*Tags:* `settings`

#### Input Parameters
* `name` - _required_ - The name of the search application to be reset.
<br />Format: applications/{application_id}.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets indexed item statistics aggreggated across all data sources.

*Tags:* `stats`

#### Input Parameters
* `fromDate.day` - _optional_ - Day of month. Must be from 1 to 31 and valid for the year and month.
* `fromDate.month` - _optional_ - Month of date. Must be from 1 to 12.
* `fromDate.year` - _optional_ - Year of date. Must be from 1 to 9999.
* `toDate.day` - _optional_ - Day of month. Must be from 1 to 31 and valid for the year and month.
* `toDate.month` - _optional_ - Month of date. Must be from 1 to 12.
* `toDate.year` - _optional_ - Year of date. Must be from 1 to 9999.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets indexed item statistics for a single data source.

*Tags:* `stats`

#### Input Parameters
* `fromDate.day` - _optional_ - Day of month. Must be from 1 to 31 and valid for the year and month.
* `fromDate.month` - _optional_ - Month of date. Must be from 1 to 12.
* `fromDate.year` - _optional_ - Year of date. Must be from 1 to 9999.
* `name` - _required_ - The resource id of the data source to retrieve statistics for,
in the following format: "datasources/{source_id}"
* `toDate.day` - _optional_ - Day of month. Must be from 1 to 31 and valid for the year and month.
* `toDate.month` - _optional_ - Month of date. Must be from 1 to 12.
* `toDate.year` - _optional_ - Year of date. Must be from 1 to 9999.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the latest state of a long-running operation.  Clients can use this<br/>
> method to poll the operation result at intervals as recommended by the API<br/>
> service.

*Tags:* `operations`

#### Input Parameters
* `name` - _required_ - The name of the operation resource.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-cloudsearch-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
