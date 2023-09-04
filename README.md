# GitHub Actions Crash Couse - Play ground

Welcome to the github action crash course playgroung! The aim of this repository is to learn how to use reusable workflow using 





## Challenges

### 1. Run a workflow locally
1. Install act  (See [How to run workflow local](#how-to-run-workflow-locally) )
2. Clone github-actions-call-reusable-workflow
3. Run locally the workflow from `/.github/workflows/challenge_1.yml`


----

### 2. Create a composite action 
1. Remove the `.tmp` extension from `challenge_2.yml.tmp`
2. Change the access permissions of the goodby script: `chmod +x goodbye.sh`
3. Modify workflow from `/.github/workflows/challenge_2.yml` to call composite action `hello_world_composite.yml`
4. Run succesfully `challenge_2.yml` workflow using act `act -j "hello_world_composite"`

See https://docs.github.com/en/actions/creating-actions/about-custom-actions#composite-actions


----

### 3. Create a simple reusable workflow
The aim of this challenge is to implement a workflow that make use of the workflow defined in:
https://github.com/XoCedillo/crashcourse-reusable-workflows/

1. Fork and clone [crashcourse-reusable-workflows](https://github.com/XoCedillo/crashcourse-reusable-workflows) repository
2. Read [README.md](https://github.com/XoCedillo/crashcourse-reusable-workflows/blob/main/README.md) to understand the structure of the reusable workflow
3. Remove the `.tmp` extension from `challenge_3.yml.tmp`
4. Modify the `github-actions-call-reusable-workflow/.github/workflows/challenge_3.yml` to call the `main.yml` reusable workflow from [main.yml](https://github.com/XoCedillo/crashcourse-reusable-workflows/blob/main/.github/workflows/main.yml) of your forked repository (See doc: https://docs.github.com/en/actions/using-workflows/reusing-workflows)
4. Run succesfully `challenge_3.yml` workflow using act `act -j "go-workflow"`



----

## How to run workflow locally

Act is a tool that allows you to run Github actions locally. To install act, go to the repository and follow the installation steps:
https://github.com/nektos/act#installation


Yo can find the corresponding documentation in:
https://nektosact.com/beginner/index.html


- To list all workflows try:
```act -l```
- To run an specific job you can try:
```act -j "<job_name>"  ```
