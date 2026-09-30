Users: 
    - id: ObjectId
    - profileImageURL: String
    - email: String,  req, unique
    - role: String, enum: ['admin', 'student']
    - profile {year: Number, department: String}
    - name: String, req
    - passwordHash: String, req 
    - createdAt: Date, req
    - updatedAt: Date, req


Backend Validation

Student

`studentId`, `year`, and `department` are required.
`year` must represent a valid college year.
Student email must belong to the college domain.

Admin

`studentId`, `year`, and `department` are not required.
Admin accounts cannot be created through normal student registration.

General

Email must be unique.
Password must be hashed before storage.
Role must never be accepted blindly from an unauthenticated registration request.
Admin will only be able to login, not signup. Signup will be handled by the backend on the database itself