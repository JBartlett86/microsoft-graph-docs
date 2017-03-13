# directory resource type (deleted items)

Represents a deleted item in the directory. When an item is deleted, it is added to the deleted items "container". 

Currently, deleted items functionality is only supported for groups. You can perform the following operations on deleted items:

* If an group was accidentally deleted, you can restore the group from deleted items. The group will be fully restored including all memberships and data.
* You can permanently delete a group from deleted items. But, once an item is permanently deleted, it cannot be restored.

Deleted items will remain available for up to 30 days. After 30 days, the items are permanently deleted.

### Methods

| Method         | Return Type | Description |
|:---------------|:------------|:------------|
|[Get deleted item](../api/directory_deleteditems_get.md) | [directoryObject](directoryobject.md) | Gets the properties of a deleted item. |
|[Restore deleted item](../api/directory_deleteditems_restore.md) |[directoryObject](directoryobject.md)| Restores a recently deleted item. |
|[List deleted items](../api/directory_deleteditems_list.md) |[directoryObject](directoryobject.md) collection| Gets a list of recently deleted items. |
|[Permanently delete an item](../api/directory_deleteditems_delete.md) | None | Permanently deletes an item. |

### Properties
| Property   | Type |Description|
|:---------------|:--------|:----------|
|id|String| A unique identifier for the object; for example, 12345678-9abc-def0-1234-56789abcde. Key. Not nullable. Read-only.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|deleteditems|[directoryObject](directoryobject.md) collection| Recently deleted groups. Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directory"
}-->

```json
{
  "id": "String (identifier)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directory resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->