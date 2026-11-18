# GovStack Building Block Template

See [GovStack Process](https://github.com/GovStackWorkingGroup/govstack-process) and [Specification Framework](https://github.com/GovStackWorkingGroup/specification-framework).

## Repo Structure

```sh
.
├── ADR
├── assets
├── authors.yml
├── introduction
│   ├── purpose.md
│   ├── scope.md
│   ├── technical_overview.md
│   ├── terminology.yml
│   └── references.md
├── requirements
│   └── functionality-name.md
├── resources
│   ├── api
│   │   ├── swagger.json
│   │   └── swagger.yaml
│   └── test
│       ├── examples
│       │   ├── exampleApp
│       │   │   ├── docker-compose.yml
│       │   │   ├── Dockerfile
│       │   │   ├── entrypoint.sh
│       │   │   ├── example-app-data.json
│       │   │   ├── README.md
│       │   │   └── test_entrypoint.sh
│       │   ├── README.md
│       │   └── someApp
│       │       ├── Caddyfile
│       │       ├── docker-compose.yaml
│       │       └── Dockerfile
│       └── openAPI
│           ├── docker
│           │   ├── Dockerfile
│           │   └── entrypoint.sh
│           ├── docker-compose.yaml
│           └── test_entrypoint.sh
├── LICENSE
├── README.md
├── CHANGELOG.md
├── RELEASE_NOTES.md
├── metadata.yml
└── toc.yml
```

