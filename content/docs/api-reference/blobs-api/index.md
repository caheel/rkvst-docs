---
title: "Blobs API"
description: "Blobs API Reference"
lead: "Blobs API Reference"
date: 2021-06-09T13:32:57+01:00
lastmod: 2021-06-09T13:32:57+01:00
draft: false
images: []
menu: 
  docs:
    parent: "api-reference"
weight: 104
toc: true
---

## Blob API Examples

Create the [bearer_token](../../setup-and-administration/getting-access-tokens-using-app-registrations) and store in a file in a secure local directory with 0600 permissions.

### Upload a Blob

Upload the blob stored at /path/to/file:

```bash
curl -v -X POST \
    -H "@$BEARER_TOKEN_FILE" \
    -H "content_type=image/jpg" \
    -F "file=@/path/to/file" \
    https://app.rkvst.io/archivist/v1/blobs
```

The response is:

```json
{
  "hash": {
    "alg": "SHA256",
    "value": "xxxxxxxxxxxxxxxxxxxxxxx"  },
  "identity": "blobs/<blob-id>",
  "issuer": "local",
  "mime_type": "image/jpeg",
  "size": 81254,
  "subject": "user@rkvst.com",
  "tenantid": "tenant/<tenant-id>",
  "timestamp_accepted": "2023-02-06T16:04:31Z",
  "scanned_status": "NOT_SCANNED",
  "scanned_bad_reason": "",
  "scanned_timestamp": ""
}
```

### Retrieve a Blob

Retrieve a specific attachment:

```bash
curl -v \
    -H "@$BEARER_TOKEN_FILE" \
    -H "content_type=image/jpg" \
    --output "/path/to/file" \
    https://app.rkvst.io/archivist/v1/blobs/08838336-c357-460d-902a-3aba9528dd22
```

The response is:

```json
{
  "hash": {
    "alg": "SHA256",
    "value": "xxxxxxxxxxxxxxxxxxxxxxx"  },
  "identity": "blobs/<blob-id>",
  "issuer": "local",
  "mime_type": "image/jpeg",
  "size": 81254,
  "subject": "user@rkvst.com",
  "tenantid": "tenant/<tenant-id>",
  "timestamp_accepted": "2023-02-06T16:04:31Z",
  "scanned_status": "NOT_SCANNED",
  "scanned_bad_reason": "",
  "scanned_timestamp": ""
}
```

## Blobs OpenAPI Docs

{{< openapi url="https://raw.githubusercontent.com/rkvst/archivist-docs/master/doc/openapi/blobsv1.swagger.json" >}}
