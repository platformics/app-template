# App-template

Inside the namespaces folder, we will have different projects that can have different manifests and charts.

In proj1 it represents applications that run in the proj1 namespace and in proj2 other applications that run in the proj2 namespace

By default, argo will deploy whatever is at the third level, that is, microservice1, and microservice2 within the proj1 namespace. If you are going to place your application here it needs to be at this level.

Nothing prevents you from pointing your project to the argo directly by creating an application for it in the argocd gui itself. This template is if you want to isolate the application manifests.

Remembering that it will only deploy what is in the main branch.
