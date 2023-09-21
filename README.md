# App-template

Inside argo folder we need an aplicationset and aplications to config this repo template.

Inside the namespaces folder, we will have different projects that can have different manifests and charts.

In proj1 it represents applications that run in the proj1 namespace and in proj2 other applications that run in the proj2 namespace.

In each proj, was created a folder named `shared` to write manifest used by all microservices in same namespace.

By default, argo will deploy whatever is at the third level, that is, microservice1, and microservice2 within the proj1 namespace. If you are going to place your application here it needs to be at this level.

Nothing prevents you from pointing your project to the argo directly by creating an application for it in the argocd gui itself. This template is if you want to isolate the application manifests.

Remembering that it will only deploy what is in the main branch.

```bash
❯ tree
.
├── argo
│   └── config.yaml
├── LICENSE
├── namespaces
│   ├── proj1
│   │   ├── microservice1
│   │   │   └── README.md
│   │   ├── microservice2
│   │   │   └── README.md
│   │   └── shared
│   │       └── README.md
│   └── proj2
│       ├── microservice1
│       │   └── README.md
│       ├── README.md
│       └── shared
│           └── README.md
└── README.md
```