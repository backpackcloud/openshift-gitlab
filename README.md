# GitLab OpenShift Template

## Prerequisites

Before applying the template, you need to add some entries in the SCC:

    oc adm policy add-scc-to-user anyuid -z default -n <namespace>
    oc adm policy add-scc-to-user anyuid -z <application-name>-user -n <namespace>
    oc adm policy add-scc-to-user privileged -z <application-name>-user -n <namespace>

The `application-name` will be passed to the template, the default value is `gitlab-ce`.
