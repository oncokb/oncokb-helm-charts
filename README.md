# OncoKB Helm Charts

These charts are customized to work with our older k8 server version (v1.11).

## Packaging charts:

Verify that our helm charts are well formed using:
```
helm lint charts/keycloak charts/elasticsearch
```

Package charts and store `.tgz` archive files inside `release/` folder: 
```
helm package charts/keycloak charts/elasticsearch -d releases/
```

Regenerate `index.yaml` file
```
helm repo index releases/
```

Go to GitHub and select `main` branch as source for GitHub Pages.

## Using charts:
```
helm repo add oncokb https://oncokb.github.io/oncokb-helm-charts/releases
```