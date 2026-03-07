# Integrate Unit Test Automation

This folder holds the files for the lab: _Integrate Unit Test Automation_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

Establish the Tasks:
kubectl apply -f tasks.yaml

The git-clone task is part of the Tekton Catalog and is indexed on Artifact Hub for discovery

Option 1: Discover via Artifact Hub and apply the raw manifest:
kubectl apply -f https://github.com/tektoncd/catalog/raw/main/task/git-clone/0.10/git-clone.yaml

Option 2: Install directly from the Tekton Catalog:
kubectl apply -f https://raw.githubusercontent.com/tektoncd/catalog/main/task/git-clone/0.9/git-clone.yaml

tkn task ls

Establish the Workspace:
kubectl apply -f pvc.yaml

Add the flake8 Task:
kubectl apply -f https://github.com/tektoncd/catalog/raw/main/task/flake8/0.1/flake8.yaml
or
kubectl apply -f https://raw.githubusercontent.com/tektoncd/catalog/main/task/flake8/0.1/flake8.yaml

