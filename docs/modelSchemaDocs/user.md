Users: 
    - id: ObjectId
    - profileImageURL: String, required
    - email: String,  req, unique
    - role: String, enum: ['admin', 'student']
    - name: String, req
    - password: String, req 
    - createdAt: Date, req
    - updatedAt: Date, req