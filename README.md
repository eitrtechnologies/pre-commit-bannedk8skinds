# pre-commit-bannedk8skinds
pre-commit hook to deny commits of certain Kubernetes object types

See also: <https://github.com/pre-commit/pre-commit>

### Using pre-commit-bannedk8skinds with pre-commit

Add this to your `.pre-commit-config.yaml`

```yaml
-   repo: https://github.com/nicholasmhughes/pre-commit-bannedk8skinds
    rev: v1.0.0  # Use the ref you want to point to
    hooks:
    -   id: bannedk8skinds
```

### Hooks Available

#### `bannedk8skinds`
Deny commits of certain Kubernetes object types. Defaults to `Secret`
  - `--allow-multiple-documents` - allow yaml files which use the
    [multi-document syntax](http://www.yaml.org/spec/1.2/spec.html#YAML)
  - `--kinds` - Specify a comma-separated list of
    [Kubernetes object types](https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds)
    which will be denied in a commit to the repo.
