# Create a base pipeline

This folder holds the files for the lab _Create a Base Pipeline_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

Apply it to the cluster:
kubectl apply -f tasks.yaml
kubectl apply -f pipeline.yaml

Run the hello-pipeline:
tkn pipeline start --showlog hello-pipeline

Run cd-pipline:
tkn pipeline start cd-pipeline \
    --showlog \
    -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git" \
    -p branch="main"

tkn task ls
tkn pipeline ls