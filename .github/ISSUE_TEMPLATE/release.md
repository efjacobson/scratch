---
name: 'Release'
title: 'scratch release vN.N.N'
about: 'Use this when deploying scratch'
---
<!-- .github/ISSUE_TEMPLATE/release.md -->
<!-- IF THERE IS A NEWER VERSION OF THIS TEMPLATE IN RELEASE-NEXT, YOU SHOULD USE THAT VERSION -->

### Click [here](#user-content-definitions) for definitions

- Decide on the [version](#user-content-definition-version). Replace any `N.N.N` text in the raw markdown of this issue with that version.
- If any ticket that will be included in this release has the `e2e` label, add the `e2e` label to this ticket.
- [ ] [Create a milestone](https://example.com) titled `scratch-vN.N.N`.
- [ ] Assign all tickets going out in this release _**including this ticket**_ to the new milestone.
- [ ] Ensure that [all tickets](https://example.com) have a detailed [QA Notes](#user-content-definition-qa-notes) _**Do not continue this process until every ticket is complete**_.
- [ ] Add this ticket to the Release Column of the [Project](https://example.com).
- [ ] Update the versions in `package.json` and `package-lock.json` by running `npm version (major|minor|patch)`.
- [ ] Run `nvm use` and `npm install`.
- [ ] Update `composer.json` with the new version.
- [ ] Run `docker compose run app composer update`.
- Ensure `CHANGELOG.md` has entries for each ticket and the correct `## vN.N.N` header.
- [ ] Commit and push changes to the release branch.
- [ ] Create a pull request for the release branch into master.
  - The __Title__ should be the new version: `vN.N.N`.
  - The __Description__ should be the same `CHANGELOG.md` notes without the `## vN.N.N` header.
- [ ] Once approved, __squash and merge__ into master and immediately [create a new release](https://example.com).
  - The __Tag version__ should be the new version: `vN.N.N`.
  - The __Target__ should be the commit of the squash merge you just did. It is likely the first one in the "Recent Commits" tab.
  - The __Release title__ should be the new version: `vN.N.N`.
  - The __Description__ should be the same `CHANGELOG.md` notes without the `## vN.N.N` header.
- Open AWS console to monitor the pipelines:
  - [link](https://example.com)
  - [link](https://example.com)
```
Subject: scratch release vN.N.N (major|minor|patch)
Body:
cool

ETA on Prod: YYYY-MM-DD
```
- [ ] Move [all tickets](https://example.com) to the [QA column](https://example.com) of the [Project](https://example.com). QA will add the `status:wip`, `status:passed`, and/or `status:failed` labels as appropriate.
- [ ] Ping __QA__ in `dev-release` channel: `@qateam scratch is ready for testing on dev/test`.

### For every ticket that fails QA: assess the situation
- Is the failure a blocker for release? Ping `@qateam`, `@product`, and the developer who did the work for the ticket and figure it out. Make new tickets and involve [SMEs](#user-content-definition-sme) as needed.
- If an [e2e](#user-content-definition-e2e) is required, determine if it has been compromised by the failure. If it must be fixed before releasing but is minor enough that QA can continue testing and come back to the issue later (after the fix has been released), they should do so. If it is a critical/low-level/global issue then they should stop, wait for the release with the fix, and start over.
- If the failure is a blocker for release open AWS console and reject the build in the pipeline for BOTH regions:
  - click the __Review__ button under the UAT card.
  - in the comments section, add the version number and short description of why build is rejected (e.g. "vN.N.N rejected due to an error doing `foo` while `bar`.")
  - click the __Reject__ button.

### If all tickets pass QA:
- If there are no `uat`, `analytics`, `adops`, `adtech`, or `legal` labels on any ticket in this release, then it does not require additional validation (i.e. you can treat it as if each ticket had immediately passed UAT).
- [ ] Move [all tickets](https://example.com) to the [UAT column](https://example.com?filterQuery=status%3A%22%F0%9F%92%AC+UAT%22).
- [ ] Notify all other stakeholder teams that need to validate the build:
- If there are any [tickets with a legal label](https://example.com+label%3Alegal+), inform the Legal team. The ticket's `Legal Notes` section will have more details.
- If there are any [tickets with a uat label](https://example.com+label%3Auat+), inform the Product team.

### For every ticket that fails UAT: assess the situation
- Is the failure a blocker for release? Contact the Product team, the stakeholder teams, and the developer who did the work for the ticket and figure it out. Make new tickets and involve SMEs as needed.
- If the failure is a blocker for release open AWS console and reject the build in the pipeline for BOTH regions:
  - click the __Review__ button under the UAT card.
  - in the comments section, add the version number and short description of why build is rejected (e.g. "vN.N.N rejected due to an error doing `foo` while `bar`.")
  - click the __Reject__ button.

### If all tickets pass UAT
- [ ] Add the `status:passed` label to [all tickets](https://example.com). Most stakeholder team members will not update labels on our board. The Product team might but you should not hesitate to do it for them if they have signed off via email, slack, etc.
- Check for __deploy notes__ label on any ticket, if label exists, confirm that all predeployment steps have been completed.
- Ask the PM or Director in the `dev-release` Slack channel if engineering is ready to go to prod. Continue only if they are ready.
- [ ] Ping __QA__ in the `dev-release` Slack channel to ask if they are ready: `@qateam scratch is ready to go to prod, are you ready?`. Continue only if they are ready.
- [ ] Remove all `status:*` labels and move tickets to the __Deploy__ column.
- Open AWS console and Approve the __UAT__ stage on both pipelines (us-west-2/us-east-1) in that order.
```
deployed to production

https://www.scratch.com/health-check/
```
- [ ] Ping QA in release channel `@qateam scratch is ready for testing in production`.
- If any stakeholder labels exists on any ticket, inform those teams that the changes have been release to production and request validation. Provide new test links.
- QA will add `status:passed` to all tickets in __Deploy__ column as they are validated.
- [ ] Once all tickets in the __Deploy__ column are marked `status:passed` by QA, close all tickets in the milestone and close the milestone.

# Definitions <a href="#user-content-definitions" id="definitions">&nbsp;</a>
- **Release**:<a href="#user-content-definition-release" id="definition-release">&nbsp;</a>Making a new code available to the world via our AWS CodePipeline.
- **e2e**:<a href="#user-content-definition-e2e" id="definition-e2e">&nbsp;</a>An end-to-end test of the entire app (as opposed to checking only the new features or bugfixes that will be included in this release).
- **Hotfix**:<a href="#user-content-definition-hotfix" id="definition-hotfix">&nbsp;</a>A release that skips much of the usual workflow process because it includes a high priority change, often a bugfix. The flow for a hotfix is roughly the same at this except the branch is created off of `master`, and merged directly back into `master` and then into `release-next`. Doing this means that any pending items that may be in `release-next` do not slow down the hotfix release.
- **Version**:<a href="#user-content-definition-version" id="definition-version">&nbsp;</a>A way to reference the code at a certain point of time. We use [semver](https://semver.org/), don't think about it too much, just follow the rules there. If _any_ of the tickets is more than a bugfix, it is a minor version. Major versions are few and far between; if you're not sure if you're doing one right now, you aren't.
- **QA Notes**:<a href="#user-content-definition-qa-notes" id="definition-qa-notes">&nbsp;</a>The section of a ticket which includes notes and instructions for our teammates in QA. This section is required and must include all required or relevant information that someone would need in order to test that the ticket does what it is supposed to do. Do not assume that the person reading these notes has the context that you do. Think of a time when you have received a poorly written ticket in the past and create the opposite experience for them.
- **UAT**:<a href="#user-content-definition-uat" id="definition-uat">&nbsp;</a>User Acceptance Testing. This comes after QA has done the first round. The Product Team and any other stakeholders will test the fix/feature as a user and decide if the experience is how they want it to be. This is a somewhat subtle and subjective step in that the release may technically accomplish everything laid out in the ticket, but if there is something that affects the experience in an unexpected and undesired way it may still be rejected.
- **Stakeholder Team**:<a href="#user-content-definition-stakeholder-team" id="definition-stakeholder-team">&nbsp;</a>One or more people who are invested in one or more of the tickets being released. AdOps, AdTech, Analytics, Legal, are common.
- **SME**:<a href="#user-content-definition-sme" id="definition-sme">&nbsp;</a>Subject Matter Expert. Someone on the team who knows a lot about something and is therefore a good person to ask questions related to said thing. If you aren't sure who is an expert, ask around.
