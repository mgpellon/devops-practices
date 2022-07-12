# Production Library and Readiness

This project contains a library of blueprints and designs, and their outcome - production readiness review.

## Overview

The Infrastructure Library contains a snapshot in time of our thinking about 
the problems we are solving. This happens through two stages:

1. We begin with **blueprints**, which define and scope a problem and provide 
options on how we might approach said problem.

2. The **design** stage, which fleshes out the approach and provides the technical 
design on the solution.

Once we have executed on the design, we create a production readiness review 
whenever there is a significant change to **<APP_NAME>** infrastructure. This may 
be a new service, a new feature, or a major infrastructure change.

After completing the readiness review, we update the relevant architectural 
and/or operational documentation.

## Getting Started

The Production Readiness Review is a process that helps identify the 
reliability needs of a service, feature or significant change to 
infrastructure for **<APP_NAME>**. It loosely follows the [production readiness 
review][prw] from the SRE book. The goal of the readiness review is to make 
sure we have enough documentation, observability, and reliability for the 
feature, change, or service to run at **<APP_NAME>** production scale.

For **<APP_NAME**>**, this review is meant to facilitate collaboration between 
Development, DevOps, and Security teams to share and help bridge any gaps about 
a new service. The review document will serve as a snapshot of what is being 
deployed and the discussions that surround it. It is not intended to be constantly 
updated.

The review starts by creating a new issue in the readiness project. After this, 
an MR is created using the example template which is the baseline for the review. 
We prefer to use an MR for reviewing the readiness document since it allows for 
inline comments, threaded discussions, and explicit assignments for review.

The readiness review MR may go through multiple rounds of review, including merges 
to mainline. It is recommended to send the first review to team members who are 
closest to the service or feature. Though most essential readiness questions 
should be captured in the template, it is fine to add more details as necessary. 
All non-applicable sections should be noted in the MR.

The readiness review needs to be approved by all required reviewers before the 
change is deployed and is taking production traffic. It is important to start 
the readiness as early as possible, as early as development and design. If it's 
not clear on what is needed to make a service scale for **<APP_NAME>**, engage 
with DevOps Team members on the design phase to receive guidance on the direction.

[prw]: https://sre.google/sre-book/evolving-sre-engagement-model/