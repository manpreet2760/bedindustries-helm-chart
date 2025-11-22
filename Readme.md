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

6. Use following set of commands to push an update to the helm repository
   1. helm plugin remove s3 
   2. helm plugin install https://github.com/hypnoglow/helm-s3.git
   3. helm package bedindustries-microservice-group/
   4. helm repo remove bedindustries
   5. helm repo add bedindustries s3://leowand-com-helm-chart/
   6. helm s3 push --force ./bedindustries-microservice-group-3.0.0.tgz bedindustries
   7. helm repo index . --url https://manpreet2760.github.io/bedindustries-helm-chart/

