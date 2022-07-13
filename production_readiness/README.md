# Production Library and Readiness

This project contains a library of blueprints and designs, and their outcome - production readiness review.

## Overview

The Infrastructure Library contains a snapshot in time of the team's thinking 
about the problems we are solving. This happens through two stages:

1. We begin with **blueprints**, which define and scope a problem and provide 
options on how we might approach said problem.

2. The **design** stage, which fleshes out the approach and provides the technical 
design on the solution.

Once we have executed on the design, we create a production readiness review 
whenever there is a significant change to **<APP_NAME>** infrastructure. This 
may be a new service, a new feature, or a major infrastructure change.

After completing the readiness review, we update the relevant architectural 
and/or operational documentation.

## Getting Started

The Production Readiness Review is a process that helps identify the 
reliability needs of a service, feature or significant change to 
infrastructure for **<APP_NAME>**. It loosely follows the [production readiness 
review][prw] from the Google SRE book. The goal of the readiness review is to 
make sure we have enough documentation, observability, and reliability for the 
feature, change, or service to run at **<APP_NAME>** production scale.

For **<APP_NAME>**, this review is meant to facilitate collaboration between 
Development, DevOps, and Security teams to share and help bridge any gaps about 
a new service. The review document will serve as a snapshot of what is being 
deployed and the discussions that surround it. It is not intended to be constantly 
updated.

## Process

The Production Readiness process is authored by the individual directly 
responsible for the work that is being delivered.

1. The author creates an issue which uses the issue template in the readiness 
project.
2. The title of the issue should be a descriptive name of change.
3. The process for the readiness review is specified in the issue in the form 
of a checklist, the instructions will guide the review author until the review 
is complete.

### Guidelines for the author

- Be as descriptive as possible when writing this review. Avoid terminology 
that make it appear as if something is already well known. What may be known
by one may not be well understood by another.

- Make no assumptions. If an answer cannot be provided, it is better to explain
why we lack the ability to provide details. This assists in fostering 
discussion and enables us to spawn new issues if we identify areas of 
improvement. This is also an excellent avenue for asking for help as needed.

### Guidelines for the reviewer

- As a reviewer of the Production Readiness proposal, your task is to 
collaborate with the author and decide whether information provided in the 
proposal is sufficient for production readiness.

- Consider how sections listed in the review template are addressed. It is 
important that you highlight any shortcomings that you observe. Ensure that
non-applicable sections are properly noted and that tickets are created if
there are any gaps that need to be addressed following the change.

[prw]: https://sre.google/sre-book/evolving-sre-engagement-model/

## Directory Structure

The directory structure of this project has

- a single directory per change. 

In each directory there will be one or more markdown documents that break 
the change into different audiences for reviews. It is not necessary to 
have more than one markdown document, it will depend on the size of the change.

### Example

```
<infrastructure change name>
  \
    - overview.md
      * architecture overview
      * deployment and timeline
      * risk assessment
      * security considers, and secrets
    - monitoring.md
      * metrics
      * logging
      * alerting
    - testing.md
      * all testing procedures 
```