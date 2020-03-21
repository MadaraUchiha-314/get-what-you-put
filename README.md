# get-what-you-put

## Specification

- Given payload it will store it in the DB and then it will serve as an API.
- There will be 2 API's:
    - POST
        - To put a json in the DB and crate a hash out of it
    - GET
        - Given a hash, return the JSON payload corresponding to the hash

## Best Practices

- Coding standards
    - Pre-Commit Hooks
        - Linting
        - Build and Unit Test
- Every Pull Request is:
    - Built
    - Unit Tested
    - Code Coverage Reported in PR
    - Functional/Integration Tested
    - Security Standards tested
- Every Merge to master:
    - All things in PR
    - Artifact is created of the build
    - Artifact is versioned and stored to "an" artifact repository
- Deployment
    - A docker image is created with the environment required for the artifact to serve request
    - The deployment is done on a Kubernetes stack
- Logging
    - All the system health metrics are logged to log server like a splunk or elastic searching
    - Dashboard for all the monitoring metrics
- Analytics
    - All the business metrics flow into a server
    - Dashboard for all the analytics metrics to be tracked
- Failure analysis
    - How does the system react when something is down ?
        - Databse is down
        - API server is down
