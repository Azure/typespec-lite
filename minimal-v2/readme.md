# {{parameters.ServiceNamespace}}

> see https://aka.ms/autorest

This is the AutoRest configuration file for {{parameters.ServiceNamespace}}.

## Getting Started

To build the SDKs for My API, simply install AutoRest via `npm` (`npm install -g autorest`) and then run:

> `autorest readme.md`

To see additional help and options, run:

> `autorest --help`

For other options on installation see [Installing AutoRest](https://aka.ms/autorest/install) on the AutoRest github page.

---

## Configuration

### Basic Information

These are the global settings for {{parameters.ServiceNamespace}}.

```yaml
openapi-type: arm
openapi-subtype: rpaas
tag: package-{{parameters.APIVersion}}
```

### Tag: package-{{parameters.APIVersion}}

These settings apply only when `--tag=package-{{parameters.APIVersion}}` is specified on the command line.

```yaml $(tag) == 'package-{{parameters.APIVersion}}'
input-file:
  - [[ReleaseState]]/{{parameters.APIVersion}}/{{#normalizePackageName}}{{parameters.ServiceNamespace}}{{/normalizePackageName}}.json
```
