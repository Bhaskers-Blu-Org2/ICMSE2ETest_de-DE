# <a name="location-resource-type"></a>location resource type

Represents location information of an event.


## <a name="properties"></a>Eigenschaften
| Eigenschaft  | Typ   | Beschreibung                                                     |
|:----------|:-------|:----------------------------------------------------------------|
| address | [physicalAddress](physicalAddress.md) |The street address of the location. |
| DisplayName  | String | Der Name der physischen Datei, die mit dem aktuellen Fehler zusammenhängt                       |



## <a name="json-representation"></a>JSON representation

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.location"
}-->
```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "location resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->