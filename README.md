# oma-docs

This is the documentation home for **OpenShift Migration Advisor (OMA)** and the migration-assessment work happening in the [kubev2v](https://github.com/kubev2v) community.

If you are planning a move from VMware toward **OpenShift Virtualization**, you are juggling inventory, risk, and timelines. OMA is meant to make that first step—**understanding what you have and what it will take to migrate**—a little less guesswork. **oma-docs** is where we write that story in one place, in language that holds up when you are not looking at a terminal or a product console.

## What this is

**oma-docs** is not another code repository with a long README. It is where we keep the **narrative**. It covers how OMA fits together, who it is for, and what people should expect when they run an assessment or read a report.

## What we are trying to do

- **Onboarding** — Take someone from “what is OMA?” to the practical next steps, including how assessments run, which surfaces to use, and where to look when you need the nitty-gritty in a service repo.

- **Alignment** — When we talk about the same concepts here as in the code, the experience feels consistent. The implementation lives in [Migration Planner](https://github.com/kubev2v/migration-planner), the [assisted migration agent](https://github.com/kubev2v/assisted-migration-agent), and the [Migration Planner UI](https://github.com/kubev2v/migration-planner-ui-app).

## What you will find here

The detailed pages will show up as we add them. For the moment, this **README** is the charter, and it says why **oma-docs** exists and how it relates to the software next door. Check back as the folders fill in.

## The software this documentation talks about

OMA is built as several pieces. **oma-docs** is the friendly signpost, and it points you to the right building when you need to *run*, *build*, or *contribute* something specific.

| Component | Repository | In practice |
| --- | --- | --- |
| **Migration Planner (service)** | [kubev2v/migration-planner](https://github.com/kubev2v/migration-planner) | The service behind storing and showing assessment results, and generating the discovery agent (including the **OVA** you deploy in VMware). The [project README](https://github.com/kubev2v/migration-planner/blob/main/README.md) describes what is collected, how the flow works, and the architecture. If you are hacking on this stack, [CONTRIBUTING](https://github.com/kubev2v/migration-planner/blob/main/CONTRIBUTING.md) is the path for **OpenShift Migration Advisor** development. |
| **Assisted migration agent** | [kubev2v/assisted-migration-agent](https://github.com/kubev2v/assisted-migration-agent) | The component that **goes to your vSphere world**, pulls the inventory and assessment data, and **phones home** to the Migration Planner console—so the picture you see in the product matches what is on the ground. |
| **Migration Planner UI** | [kubev2v/migration-planner-ui-app](https://github.com/kubev2v/migration-planner-ui-app) | The **React/TypeScript** app where many people will **see** assessments and planning flows. The [UI README](https://github.com/kubev2v/migration-planner-ui-app/blob/master/README.md) has the quick start, how to build, and pointers to contributing, local dev, and version details. |

## More resources

- The rest of the [kubev2v](https://github.com/kubev2v) org—sibling projects around migration and virtualization.
- The **OpenShift Migration Advisor** / **migration-advisor** documentation that ships with the product, when you need the polished, customer-facing site. This repo is where we **draft and version** the narrative in step with the code, so the two can stay friends.

If something here is wrong, outdated, or missing, open an issue or a pull request. Good documentation is a conversation, not a monument.
