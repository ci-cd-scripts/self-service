# self-service

[![IssueOps Handler](https://github.com/ci-cd-scripts/self-service/actions/workflows/issueops.yml/badge.svg)](https://github.com/ci-cd-scripts/self-service/actions/workflows/issueops.yml)

---

## :wave:  Introduction

**self-service** is an **open-source collection of GitHub Org & Enterprise automations** that leverage **IssueOps**.

### Why?

> 1. As a developer starting projects often, you want to have a reliable way to quickly create and manage them.
> 2. As an Org Owner, you want to scalably manage your Org by making app team requests instant & secure.
> 3. As an Enterprise Owner, you need to adhere to certain controls and audit requirements and can't afford to become a bottleneck to your developers.

### What is this repository for?

> - Automate features not yet available in GitHub
> - App teams can complete DevOps services on-demand using IssueOps
> - Add more access granularity

### What can I do?

> - Create a new repository and add team permissions based on a template.

## :clipboard:  Rules
This repo enforces the following standards and naming conventions for this Org

### General
- You must be an Org member for these requests to complete
### Teams
- A `Team` will have a GitHub team created for each repository role
  > `Admin, Maintain, Write, Triage, Read`
- Each Org has secret `Org` teams with access to all repos in the Org
### Repositories
- The secret `Org` teams are added to all new repos
  > `Org Admin, Org Maintain, Org Write, Org Triage, Org Read`
- The requester of a new repo must be a member of at least 1 `Admin` team in the request

## :checkered_flag:  Start Requesting
1. Click the Issues tab above
2. Click [`New Issue`](../../issues/new/choose)
3. Choose an automation from the available issue templates

## Coming Soon
See current states of accepted issues in the [Self-Service Features](../../milestone/2) Milestone
### :building_construction:  In Progress
#### [#10](../../issues/10): Replace `machine-learning-apps/actions-app-token` action with `github-script`
#### [#9](../../issues/10): Post-Run Job

### :bulb:  Ideas
#### :sparkle:  ServiceNow Integration
Add an _optional_ workflow to sync data between GitHub & ServiceNow
- Utilize existing data
- Keep your CMDB / SCLM up-to-date
- Enforce current policies already being used
- Keep your Github Enterprise in sync with your SCLM

#### :sparkle:  Automated GitHub App creation
Create a GitHub App for each Business App defined in ServiceNow.  
*i.e. Name: "SN Business App#"*
- Acts as a "service account"
- Tracks repo ownership
using `Select Repos` list on `https://github.com/organizations/{org}/settings/installations/{id}`
- Granular access auditable per app/team

***Security Considerations***
- Add app team members as app managers
  - **Risk**: App teams could request too much access
  - **Remediation**: All App access must be approved by an Org Owner. Apps requesting too much access can be declined or exceptions can be made and the app added to a more thorough watch-list