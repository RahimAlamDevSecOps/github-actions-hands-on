# GitHub Actions hands-on
## Concepts
## 1. Workflows
To create a GitHub Actions workflow you need a folder called `.github/workflows`

# Concepts of Github Actions Workflow
Workflow [No indentation required for naming the workflow]
Should have `Name`
name: Hello
On tells when the workflow should run (Give indentation by Tab)
on:
  workflow_dispatch:
    

## Jobs
Should be inside `Workflow`
job tells what workflow should do. There can be one or more than one jobs, hence we write jobs.
jobs is an object so need indentation. 
jobs:
  ## 1st job (Give indentation)
  say-hello:
    ## Creates an emphemeral container with Ubuntu running. (Means last only for a short time, means once the task finish it will delete automatically.)
    runs-on: ubuntu-latest
    ## That emphemeral container will have Steps to execute, hence name thos Steps and use run: run has the command.
    steps:
      - name: say hello to everyone
        run: echo "Hello Doston"

## Steps
Should be inside `Jobs`

## Actions
Should be inside `Steps`


## GitHub Actions CICD Workflows Concepts
name: CIDC 

on: 
  workflow_dispatch:

jobs:
  code:
    runs-on: ubuntu-latest
    steps:
      - name: Clone the code
        run: echo "Cloning the code"
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Build using docker
        run: echo "Building using docker"
  
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Running test cases
        run: echo "Testing the app"
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Deploying on the machine
        run: echo "Deploying the code"
