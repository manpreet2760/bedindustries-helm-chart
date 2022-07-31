## Create / Manage new Helm chart

1. helm create <chart-name>
https://helm.sh/docs/helm/helm_create/

2. helm package <chart-path>

3. Check if helm s3 plugin is installed and initialized
https://github.com/hypnoglow/helm-s3

4. Push the new chart to the repo
helm s3 push <packaged-chart> <repo-name>

5. Helm repo list
helm repo list

