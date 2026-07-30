# Documentation for the OpenShift migration advisor (OMA)

This is the documentation home for **the OpenShift migration advisor (OMA)** and automated-report initiatives within the kubev2v community.

OMA is a web-based service available on the Red Hat Hybrid Cloud Console designed to evaluate vCenter environments for migration. If you are planning a move from VMware toward OpenShift Virtualization, OMA serves as an analytical wizard to help you understand your current inventory, identify technical risks, and estimate migration timelines.

The oma-docs repository is where we maintain the narrative. It covers how OMA fits together, who it is built for, and what users should expect when they generate an automated migration report.
## What this is
**oma-docs** is not another code repository with a long README. It is where we keep the **narrative**. It covers how OMA fits together, who it is for, and what people should expect when they generate an automated migration report or read one.

## What we are trying to do

This repository focuses on bridging the gap between the source code and the user experience. Our goals are:

* **Onboarding:** Take users from learning "What is OMA?" to practical next steps, including how automated discovery processes run and how to interpret automated migration report results.  
* **Managing Expectations:** Clearly communicate that OMA provides insights, capacity plans, and time requirements that are estimations for planning purposes, not guarantees.  
* **Alignment:** Ensure that the concepts we discuss here match the implementation found across the Migration Planner, the agent, and the UI, creating a consistent experience.

The implementation lives in

* [Migration Planner](https://github.com/kubev2v/migration-planner)
* [Assisted migration agent](https://github.com/kubev2v/assisted-migration-agent)
* [Migration Planner UI](https://github.com/kubev2v/migration-planner-ui-app).

## Target audience

OMA is optimized for self-service use by VMware administrators and IT architects. The guided experience requires very little technical expertise and no prior OpenShift experience to generate the initial automated migration report. It is designed to support environments of varying sizes, smoothly handling assessments from standard deployments up to large enterprise estates.

## What you will find here

The detailed pages will show up as we add them. For the moment, this **README** is the charter, and it says why **oma-docs** exists and how it relates to the software next door. Check back as the folders fill in.

## The software this documentation talks about

OMA is built using several distinct pieces. When you need to dive into the technical details, run a service, or contribute to the code, refer to the specific repositories below:

| Component | Repository | In practice |
| --- | --- | --- |
| **Migration Planner (service)** | [kubev2v/migration-planner](https://github.com/kubev2v/migration-planner) | The service behind storing and showing automated migration report results, and generating the discovery agent (including the **OVA** you deploy in VMware). The [project README](https://github.com/kubev2v/migration-planner/blob/main/README.md) describes what is collected, how the flow works, and the architecture. If you are hacking on this stack, [CONTRIBUTING](https://github.com/kubev2v/migration-planner/blob/main/CONTRIBUTING.md) is the path for **the OpenShift migration advisor** development. |
| **Assisted migration agent** | [kubev2v/assisted-migration-agent](https://github.com/kubev2v/assisted-migration-agent) | The component that **goes to your vSphere world**, pulls the inventory data used for automated migration reports, and **phones home** to the Migration Planner console—so the picture you see in the product matches what is on the ground. |
| **Migration Planner UI** | [kubev2v/migration-planner-ui-app](https://github.com/kubev2v/migration-planner-ui-app) | The **React/TypeScript** app where many people will **see** automated migration reports and planning flows. The [UI README](https://github.com/kubev2v/migration-planner-ui-app/blob/master/README.md) has the quick start, how to build, and pointers to contributing, local dev, and version details. |

## More resources

- The rest of the [kubev2v](https://github.com/kubev2v) org—sibling projects around migration and virtualization.
- **The OpenShift migration advisor** / **migration-advisor** documentation that ships with the product, when you need the polished, customer-facing site. This repo is where we **draft and version** the narrative in step with the code, so the two can stay friends.

## Get involved

If something here is wrong, outdated, or missing, open an issue or a pull request. Good documentation is a conversation, not a monument.
