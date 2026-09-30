Claim:
    - id: ObjectId, req
    - userId: ObjectId, req
    - matchId: ObjectId, req
    - evidence: {comment: {String, req}, identifyingDetails: {String, req}, imageURLs: [String] }
    - status: String, enum: ['pending', 'accepted', rejected], req
    - createdAt: Date, req
    - updatedAt: Date, req

Backend Validation

`matchId` must reference an existing match.
`userId` must reference the user submitting the claim.
Only the claimant can create a claim for themselves.
A claim can only be submitted for an appropriate active match.
A user cannot submit multiple active claims for the same match.
`imageURLs` are optional.
New claims start with `status = 'pending'`.
Only an authorized reviewer/admin can accept or reject a claim.
`reviewedBy` is required once a claim has been reviewed.
An accepted claim should result in the associated report being eligible for resolution.