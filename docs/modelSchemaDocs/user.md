Users: 
    - id: ObjectId
    - profileImageURL: String, required
    - email: String,  req, unique
    - role: String, enum: ['admin', 'student']
    - profile {year: Number, department: String}
    - name: String, req
    - password: String, req 
    - createdAt: Date, req
    - updatedAt: Date, req