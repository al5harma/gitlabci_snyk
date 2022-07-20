# gitlabci_snyk
Repo for configs for integrating Snyk Scans with Gitlab CI

GitlabCI <> Snyk integration demo
Repo to hold templates for GitlabCI config.yml files to work with Snyk security scans.

Elaborate doc here - WIP

**Pre-requisite**

1. Setup Gitlab
2. Fork NodeJS-goof - https://github.com/snyk-labs/nodejs-goof

**Snyk.io Steps**

1. Setup a service account or use your account token for Snyk Authentication in GitlabCI

**GitlabCI Steps**

1. Project Settings --> CICD --> Pipeline Editor
2. Click Configure Pipeline 
	a. Paste app appropriate config into the yml
      - Snyk Test, Monitor, or conditional Snyk scans (snyk-delta etc.)
	
**Set the Environment Variable**

1. Project Settings 
2. CICD --> Environment Variable
    a. Add variable
    b. Snyk Auth Token (Service Account) -> SNYK_TOKEN

**Configuration Files**

There are configuration templates posted in the configuration folder.

1. Use and save the template in CICD --> Editor 
  a. Everytime you commit you will trigger a pipeline job so make sure to add SNYK_TOKEN variable beforehand.
2. Note the templates only have node dependencies for scanning goof (nodejs-goof) project as found here - https://github.com/snyk-labs/nodejs-goof
3. Please modify if you would like to scan other Snyk-lab projects.
