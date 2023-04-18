# redhat-app-mod-workshop

## Cluster Admin Authentication
As a quick example, you can execute the following to learn more about what a Role is:

oc explain Role
Inspect how ClusterRole differs:

oc explain ClusterRole
You can execute the following to learn more about RoleBinding:

oc explain RoleBinding
Inspect how ClusterRoleBinding differs:

oc explain ClusterRoleBinding
You can always use oc explain [RESOURCE] to get more explanation about what various objects are.

```
[~] $ oc get clusterrole cluster-admin -o yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRole
metadata:
  annotations:
    rbac.authorization.kubernetes.io/autoupdate: "true"
  creationTimestamp: "2023-04-18T05:38:18Z"
  labels:
    kubernetes.io/bootstrapping: rbac-defaults
  name: cluster-admin
  resourceVersion: "102"
  uid: 7a5d44f1-f7fb-4c3e-8e96-d595c39d9de1
rules:
- apiGroups:
  - '*'
  resources:
  - '*'
  verbs:
  - '*'
- nonResourceURLs:
  - '*'
  verbs:
  - '*'
```
