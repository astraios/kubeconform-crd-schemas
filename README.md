# Kubeconform CRD additional schemas

## What

This repository contains some CRDs that got formatted from their original `OpenAPI.spec` to a JSON Schema 
that can be used by `kubeconform` to check conformance of Kubernetes manifests.

## Usage

```shell
kubeconform -summary -output json \
  -schema-location default \
  -schema-location 'https://raw.githubusercontent.com/astraios/kubeconform-crd-schemas/main/crdSchemas/{{ .ResourceKind }}_{{ .ResourceAPIVersion }}.json' \
  path/to/your/manifests
```

## Credits

Huge thanks to
- https://github.com/yannh/kubeconform
- https://github.com/datreeio/CRDs-catalog
