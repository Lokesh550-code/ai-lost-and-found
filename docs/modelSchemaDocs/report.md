Report:
    - id: ObjectId, req
    - type: String, enum: ['lost', 'found'], req
    - userId: ObjectId, req
    - details: [{brand: String}, {itemName: String, req}, {color: String}, {category: String, req}, {time: Date, enum:[lostTime, foundTime], req}, {location: String, req}, {itemImageURL: String, req}]
    - resolved: Bool, req
    - createAt: Date, req
    - updateAt: Date, req