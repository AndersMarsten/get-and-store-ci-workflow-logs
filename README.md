# get-and-store-ci-workflow-logs
PoC for storing the complete CI workflow run logs with a unique version matching the produced CI artifact. 

The goal is to fetch the whole CI workflow run logs after completion of the CI workflow run or as the final step of the CI workflow.

The intention is that the later CD workflow (production deployment workflow) that is manually triggered upon demand with input as version number will fetch and use the associated logs from the CI workflow that created the deployment artefact with a specific version that is about to be deployed.

The key here is to make sure that the created binary which are push and tag to GitHub packages with a unique version tag later can be associate with the actual workflow logs that created the binary. This idea is to use the version identifier as part of the name of the log file that is stored as a separate artefact. 
 
