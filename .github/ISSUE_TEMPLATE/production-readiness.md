---
name: Production Readiness
about: Describe this issue template's purpose here.
title: ''
labels: ''
assignees: ''

---

For any new or changes to a feature or service in production, the questions in this guide will help to make these changes more robust when they are enabled on **<APP_NAME>**.

**This issue serves as a tracking issue to guide you through the readiness review. It's not the production readiness document itself!.**

**The readiness documentation will be added to the project with a merge request, where different interested parties can collaborate.**

### Readiness MR

Add link to the readiness MR when it is created

### Reviewers

The reviewers should be filled in as one of the steps of the checklist below.
If a reviewer in the "Mandatory" section is not allocated, please add the 
reason why next to the name.

#### Mandatory

[] Reliability: reviewer name
[] Delivery: reviewer name
[] Security: reviewer name

#### Optional

Delete these reviewers if they do not apply

[] Development: reviewer name
[] Database: reviewer name

### Readiness Checklist

The following items should be completed by the person initiating the 
readiness review:

[] Create an issue and assign it to yourself. Set a due-date for when you 
believe the readiness will be completed (this can be updated later if 
necessary).

[] In the "Reviewers" section above, add the reviewer names. Names will be 
assigned by reaching out to the engineering manager of the corresponding team.

[] Create the first draft of the readiness review by copying the template below 
and submitting an MR.

[] Add a link to the MR in the "Readiness MR" section at the top of this issue.

[] Assign the initial set reviewers to the MR. There can be multiple iterations 
of MR if needed, often it is helpful to have the first draft reviewed by team 
members in the same team. Approval of the MR does not mean the readiness 
document is approved, approvals will be done later on this issue.

[] When last review of the MR is complete, ask the reviewers in the "Reviewers" 
section above to check the box next to their name if they are satisfied with 
the review and have no more questions or concerns.