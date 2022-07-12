# Production Readiness

For any new or changes to a feature or service in production, the questions in 
this guide will help to make these changes more robust when they are enabled 
on **<APP_NAME>**.

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
