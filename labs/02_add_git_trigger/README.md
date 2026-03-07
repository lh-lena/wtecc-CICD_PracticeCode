# Adding GitHub Triggers

This folder holds the files for the lab: _Adding GitHub Triggers_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

Apply the EventListener resource to the cluster:
kubectl apply -f eventlistener.yaml
tkn eventlistener ls

Start a Pipeline Run
kubectl port-forward service/el-cd-listener  8090:8080
curl -X POST http://localhost:8090 \
  -H 'Content-Type: application/json' \
  -d '{"ref":"main","repository":{"url":"https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode"}}'
tkn pipelinerun ls
tkn pipelinerun logs --last