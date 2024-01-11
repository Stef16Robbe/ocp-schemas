# ocp-schemas
ocp and k8s yaml schemas in json

## notes

- installed: https://github.com/yannh/kubeconform
- downloaded the schemas using: https://github.com/datreeio/CRDs-catalog/blob/main/Utilities/crd-extractor.sh
- then ran:

```shell
kubeconform -summary -verbose -strict -ignore-missing-schemas -output pretty -schema-location default -schema-location '/Users/srobbe/.datree/crdSchemas/{{ .ResourceKind }}_{{ .ResourceAPIVersion }}.json' .
```

This works for everything except Kustomize
