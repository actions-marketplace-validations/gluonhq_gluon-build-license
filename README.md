# gluon-build-license

This action configures the license for your Gluon build

Have a look at [Hello Gluon CI](https://github.com/gluonhq/hello-gluon-ci) for a sample.

# Usage

* Add this before your Maven build step

```yaml
steps:
- name: Gluon Build License
    uses: gluonhq/gluon-build-license@v1
    with:
      gluon-license: ${{ secrets.GLUON_LICENSE }} 
```

In case, you have a multi-module setup, with `main-module` containing Gluon Application,
`dir` can be specified:

```yaml
steps:
- name: Gluon Build License
    uses: gluonhq/gluon-build-license@v1
    with:
      gluon-license: ${{ secrets.GLUON_LICENSE }}
      dir: main-module
```

* Configure GLUON_LICENSE in your repo secrets
