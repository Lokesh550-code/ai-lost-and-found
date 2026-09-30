Match:
    - id: ObjectId
    - lostReportId: ObjectId, req
    - foundReportId: ObjectId, 
    - confidenceScore: Number, min: 0, max: 1, req
    - status: String, enum: ['suggested', 'accepted', 'rejected']
    - reviewedBy: ObjectId
    - createdAt: Date, req
    - updatedAt: Date, req

 Backend Validation

`lostReportId` must reference an existing lost report.
`foundReportId` must reference an existing found report, and if not found then it can be empty until something is found.
A match cannot reference the same report on both sides.
`confidenceScore` must be within the defined range.
A match can only exist between one lost and one found report.
Duplicate matches between the same lost/found reports should not be created.
AI creates matches with `status = 'suggested'`.
Only authorized users/admins may change match status.