Claim:
    - id: ObjectId, req
    - userId: ObjectId, req
    - details: [{brand: String}, {itemName: String, req}, {color: String}, {category: String, req}, {losttime: Date, req}, {location: String, req}, {comment: String, req}, {itemImageURL: String, req}]
    - status: String, enum: ['accepted', rejected], req
    - createAt: Date, req
    - updateAt: Date, req