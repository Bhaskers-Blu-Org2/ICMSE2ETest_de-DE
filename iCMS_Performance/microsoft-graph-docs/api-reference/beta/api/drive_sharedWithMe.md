# <a name="list-items-shared-with-the-signed-in-user"></a>List items shared with the signed-in user

List the set of items that are shared with the current user.

## <a name="prerequisites"></a>Voraussetzungen
One of the following **scopes** is required to execute this API:

  * Files.Read

## <a name="http-request"></a>Verwenden Sie diese HTTP-Anforderung

<!-- { "blockType": "ignored" } -->
```
GET /me/drive/sharedWithMe
```

## <a name="request-headers"></a>Anforderungsheader

| Name          | Typ   | Beschreibung                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Autorisierung | string | Bearer <token>. Required.                                                                                                                                                                         |

## <a name="request-body"></a>Anforderungstextkörper
Do not supply a request body for this method.

## <a name="example"></a>Beispiel

<!-- { "blockType": "request", "name": "drive-sharedwithme", "scopes": "files.read" } -->
```http
GET /me/drive/sharedWithMe
```

## <a name="response"></a>Antwort

This returns a collection of [driveItem resources](../resources/driveitem.md) that contains items which have been shared with the signed-in user.


<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "isCollection": true, "truncated": true } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "1312abc",
      "remoteItem": {
        "id": "1991210caf!192",
        "name": "March Proposal.docx",
        "file": { },
        "size": 19121,
        "parentReference": {
          "driveId": "1991210caf",
          "id": "1991210caf!104"
        }
      }
    },
    {
      "id": "1312def",
      "remoteItem": {
        "id": "1991210caf!1991",
        "name": "Team Roster.xlsx",
        "file": { },
        "size": 37619,
        "parentReference": {
          "driveId": "1991210caf",
          "id": "1991210caf!104"
        }
      }
    }
  ]
}
```

## <a name="remarks"></a>Hinweise

DriveItems returned from the **sharedWithMe** action will always include the **remoteItem** facet which indicates they are items from another drive. To access the original driveItem object, you will need to make a request using the information provided in **remoteItem** in the following format:

<!-- {"blockType": "ignored"} -->
```http
GET /drives/<remoteItem.driveId>/items/<id>
```

<!-- {
  "type": "#page.annotation",
  "description": "Retrieve a list of files shared with the signed-in user.",
  "keywords": "sharedWithMe onedrive shared files",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Shared with me"
} -->
