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

- [ ] Reliability: reviewer name
- [ ] Delivery: reviewer name
- [ ] Security: reviewer name

#### Optional

Delete these reviewers if they do not apply

- [ ] Development: reviewer name
- [ ] Database: reviewer name

### Readiness Checklist

The following items should be completed by the person initiating the 
readiness review:

- [ ] Create an issue and assign it to yourself. Set a due-date for when you 
believe the readiness will be completed (this can be updated later if 
necessary).

- [ ] In the "Reviewers" section above, add the reviewer names. Names will be 
assigned by reaching out to the engineering manager of the corresponding team.

- [ ] Create the first draft of the readiness review by copying the template below 
and submitting an MR.

- [ ] Add a link to the MR in the "Readiness MR" section at the top of this issue.

- [ ] Assign the initial set reviewers to the MR. There can be multiple iterations 
of MR if needed, often it is helpful to have the first draft reviewed by team 
members in the same team. Approval of the MR does not mean the readiness 
document is approved, approvals will be done later on this issue.

- [ ] When last review of the MR is complete, ask the reviewers in the "Reviewers" 
section above to check the box next to their name if they are satisfied with 
the review and have no more questions or concerns.

### Readiness MR Template

Expand the section below to view the readiness template, this will be the starting point for the readiness merge request.

**Create `<name>/index.md` as a new merge request with the following content where <name> is something short and descriptive for the change being proposed**

<details>

_While it is encouraged for parts of this document to be filled out, not all of the items below will be relevant. Leave all non-applicable items intact and add the reasons for why in place of the response._
_This Guide is just that, a Guide. If something is not asked, but should be, it is strongly encouraged to add it as necessary._

## Summary

- [ ] **Provide a high level summary of this new product feature. Explain how this change will benefit the product's customers. Enumerate the customer use-cases.**
- [ ] **What metrics, including business metrics, should be monitored to ensure will this feature launch will be a success?**

## Architecture

- [ ] **Add architecture diagrams to this issue of feature components and how they interact with existing application components. Include internal dependencies, ports, security policies, etc.**
- [ ] **Describe each component of the new feature and enumerate what it does to support customer use cases.**
- [ ] **For each component and dependency, what is the blast radius of failures? Is there anything in the feature design that will reduce this risk?**
- [ ] **If applicable, explain how this new feature will scale and any potential single points of failure in the design.**

## Operational Risk Assessment

- [ ] **What are the potential scalability or performance issues that may result with this change?**
- [ ] **List the external and internal dependencies to the application (ex: Redis, MySQL, etc) for this feature and how the it will be impacted by a failure of that dependency.**
- [ ] **Were there any features cut or compromises made to make the feature launch?**
- [ ] **List the top three operational risks when this feature goes live.**
- [ ] **What are a few operational concerns that will not be present at launch, but may be a concern later?**
- [ ] **Can the new product feature be safely rolled back once it is live, can it be disabled using a feature flag?**
- [ ] **Document every way the customer will interact with this new feature and how customers will be impacted by a failure of each interaction.**
- [ ] **As a thought experiment, think of worst-case failure scenarios for this product feature, how can the blast-radius of the failure be isolated?**

## Database

- [ ] **If we use a database, is the data structure verified and vetted by the DBA?**
- [ ] **Do we have an approximate growth rate of the stored data (for capacity planning)?**
- [ ] **Can we age data and delete data of a certain age?**

## Security and Compliance

- [ ] **Were the organization's security development guidelines followed for this feature?**
- [ ] **If this feature requires new infrastructure, will it be updated regularly with OS updates?**
- [ ] **Has effort been made to obscure or elide sensitive customer data in logging?**
- [ ] **Is any potentially sensitive user-provided data persisted? If so is this data encrypted at rest?**
- [ ] **Is the service subject to any regulatory/compliance standards? If so, detail which and provide details on applicable controls, management processes, additional monitoring, and mitigating factors.**

