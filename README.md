# Helm Charts for public


## Lint charts

```bash
helm lint charts/*
```


## Charts

### Add repository by URL

```bash
helm repo add schamane-charts https://schamane.github.io/charts/
```

or upgrade repo

```bash
helm repo update
```


### hetzner-pvc

Mount hetzner volume as pvc by id, use values.yaml with own configuration for volume

```yaml
volumeHandle: 'xxxxxxxxx'
size: 10Gi
```

```bash
helm install -n namespace -f values.yaml test-pvc schamane-charts/hetzner-pvc
```
