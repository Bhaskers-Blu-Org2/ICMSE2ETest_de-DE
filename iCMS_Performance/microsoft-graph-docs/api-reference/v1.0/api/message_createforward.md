# <a name="message-createforward"></a>message: createForward

Create a draft of the Forward message. You can then [update](../api/message_update.md) or [send](../api/message_send.md) the draft.

## <a name="prerequisites"></a>Voraussetzungen
One of the following **scopes** is required to execute this API: *Mail.ReadWrite*
## <a name="http-request"></a>Verwenden Sie diese HTTP-Anforderung
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/<id>/createForward
POST /users/<id | userPrincipalName>/messages/<id>/createForward
POST /me/mailFolders/<id>/messages/<id>/createForward
POST /users/<id | userPrincipalName>/mailFolders/<id>/messages/<id>/createForward
```
## <a name="request-headers"></a>Anforderungsheader
| Name       | Typ | Beschreibung|
|:---------------|:--------|:----------|
| Autorisierung  | string  | Bearer <token>. Required. |
| contentType | string  | Nature of the data in the body of an entity. Required. |

## <a name="request-body"></a>Anforderungstextkörper

## <a name="response"></a>Antwort
If successful, this method returns `201, Created` response code and [Message](../resources/message.md) object in the response body.

## <a name="example"></a>Beispiel
Here is an example of how to call this API.
##### <a name="request"></a>Anforderung
Nachfolgend finden Sie ein Beispiel für das Markup des Nummerierungsteils.
<!-- {
  "blockType": "request",
  "name": "message_createforward"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/<id>/createForward
Content-type: application/json
Content-length: 248

{
  "comment": "Comment-value",
  "toRecipients": [
    {
      "emailAddress": {
        "address": "address-value"
      }
    },
    {
      "emailAddress": {
        "address": "address-value"
      }
    }
  ]
}
```

##### <a name="response"></a>Antwort
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: createForward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
