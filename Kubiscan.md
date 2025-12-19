KubiScan is used to find risky Kubernetes RBAC permissions (who can do what, privilege escalation paths, anonymous access, etc.). <br>

### What KubiScan does (quick)

KubiScan analyzes: <br>
- Roles / ClusterRoles
- RoleBindings / ClusterRoleBindings
- ServiceAccounts

And answers: <br>
- Who can become cluster-admin?
- Who can exec into pods?
- Who can read secrets?
- Privilege escalation paths

### Run basic scan using docker:

```
docker run --rm \
  -v ~/.kube:/root/.kube \
  cyberark/kubiscan
```
