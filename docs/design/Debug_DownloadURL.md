# Debug content Download URL Exposure Design

<!-- _Note_: The preferred style for design documents is one sentence per line.
*Do not wrap lines*.
This aids in review of the document as changes to a line are not obscured by the reflowing those changes caused and has a side effect of avoiding debate about one or two space after a period. -->

## Abstract
We want to provide a way for Non Admins (NAs) to debug their non admin backup (NAB) and/or non admin restore (NAR).

## Background
A backup/restore operation may not always succeed in part, or in full. User would like a way to diagnose their backup or restore based on information available on object store uploaded by Velero during its backup or restore process.

## Goals

- Make available a path or url to debug information on NAB and NAR statuses which allows credentialed user of object store to access debug information.

## Non Goals

- Create a CLI
- Automatically retrieve debug information on behalf of the user

## High-Level Design



## Detailed Design

A detailed design describing how the changes to the product should be made.

The names of types, fields, interfaces, and methods should be agreed on here, not debated in code review.
The same applies to changes in CRDs, YAML examples, and so on.

Ideally the changes should be made in sequence so that the work required to implement this design can be done incrementally, possibly in parallel.

## Alternatives Considered

Generating a short lived signed url

- While this approach do not require user to have bucket credentials, the URL retrieved will be short lived such that it will only be practical to use if programmatically used by a CLI, which is out of scope of current design.

## Security Considerations

We will assume that user who have object store credentials are the authorized personnel to access this data path and the object store bucket as a whole.
Other users who share this bucket are also assumed to be similarly privileged and have access to all other shared users data in the object store.

## Compatibility

A new status field(s) will need to be added to NAB/NAR to expose debug info path.

## Implementation
<!-- A description of the implementation, timelines, and any resources that have agreed to contribute. -->

## Open Issues
<!-- A discussion of issues relating to this proposal for which the author does not know the solution. This section may be omitted if there are none. -->
