Report:
    - id: ObjectId, req
    - type: String, enum: ['lost', 'found'], req
    - userId: ObjectId, req
    - details: [{brand: String}, {itemName: String, req}, {comment: String, req}, {color: String}, {category: String, req}, {occuredAt: Date, req}, {location: String, req}, {itemImageURL: [String]}]
    - resolved: Bool, req
    - createAt: Date, req
    - updateAt: Date, req

Backend Validation

 `itemName`, `category`, `comment`, `occurredAt`, and `location` are required for all reports.
 `itemImageURLs` is required when `type = 'found'`.
 `itemImageURLs` is optional when `type = 'lost'`.
 A student can only modify their own unresolved reports.
 `resolved` can only be changed by an admin.
 A resolved report cannot be modified by a student.
 `resolved` should only become `true` after the admin confirms that the item has been returned to its owner.