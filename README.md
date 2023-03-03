# Threat Agent GihHub Action
GitHub action for scan repository using threat-agent docker image. 
Can be incorporated in GitHub workflow as a separate step or as a part of reusable workflow. 
See example below.

```yaml
jobs:
  scan-repository:
    uses: threatrix/threat-agent-scan/.github/workflows/scan-repo-reusable.yaml@master
```

### Required parameters for action:
* eid -  EntityID: from user profile
* oid -  OrganizationID from user profile
* server-url - Threatrix API url
* api-token - API Key: from user profile
* scm-token: - SCM authorization token
* app-name - Project Name
* branch - Current branch

### Required parameters for reusable workflow:
* eid -  EntityID: from user profile
* oid -  OrganizationID from user profile

### This workflow requires to setup following secrets:
* TOKEN - GitHub toket for target repository
* THREATRIX_SERVER_API_KEY - API Key: from user profile