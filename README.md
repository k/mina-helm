# Coda Helm Charts

This is an unofficial registry of [Coda](https://coda.org/) [helm](https://helm.sh/) charts.

## Prerequisites
* [Helm](https://helm.sh/) 3+

## Setup

Add the coda helm repo:
```
helm repo add coda https://k.github.io/coda-helm
helm repo update
```

Then configure a values.yaml for the chart you want to install.

## List of Charts

### [coda](./charts/coda)

Chart to run a Coda Full Node

## Deploy to Github Pages

Deploy requires [`cr`](https://github.com/helm/chart-releaser) tool 

### Enable Github Pages (only first time)

Settings > Options > Github Pages > Source > Select master branch

### Package chart

```
helm package charts/<chart-to-package> --destination .deploy
```

### Upload New Release

```
cr upload --config config.yaml --token <deploy-token>
```

### Generate new index
```
cr index --config config.yaml
git add index.yaml
git commit -m "Update index.yaml"
git push
```
