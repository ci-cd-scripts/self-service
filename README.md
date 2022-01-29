# self-service

[![IssueOps Handler](https://github.com/ci-cd-scripts/self-service/actions/workflows/issueops.yml/badge.svg)](https://github.com/ci-cd-scripts/self-service/actions/workflows/issueops.yml)

## :building_construction: In Progress :building_construction:
### [#10](../../issues/10): Replace machine-learning-apps/actions-app-token action with github-script  

## :bulb: Ideas :bulb: 
### :desktop_computer: Automated GitHub App creation  
Create a GitHub App for each Business App defined in Service-Now.  
*i.e. Name: "SN Business App#"*  
- Acts as a "service account"  
- Tracks repo ownership  
using `Select Repos` list on `https://github.com/organizations/{org}/settings/installations/{id}`  
- Granular access auditable per app/team  

***Security Considerations***  
- Add app team members as app managers  
  - **Risk**: App teams could request too much access  
  - **Remediation**: All App access must be approved by an Org Owner. Apps requesting too much access can be declined or exceptions can be made and the app added to a more thorough watch-list