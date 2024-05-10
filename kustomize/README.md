# Kustomize

Create manifests with:

    kustomize build deployment-example/overlays/dev
    kustomize build deployment-example/overlays/prod

Use kubectl to apply to cluster with:

    kubectl apply -k deployment-example/overlays/dev

## Notes:
- Targets can be set for patch file explicitly or implicitly
- Names of parent folders base and overlays are just conventions
- In dev config patching was set implicitly by matching the fields of the base file
- In prod config pathcing was set explicitly by assigning the patch file and specifying the paths and operations
