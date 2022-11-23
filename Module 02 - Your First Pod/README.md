# Module 02 - Your First Pod

## Module Overview

OpenShift provides the best developer experience of any Kubernetes distribution available today, and getting your first pod up and running is probably the best way to show what we're talking about.

In this lab, we will deploy an app using an existing container image. OpenShift will create an image stream for the image, as well as deploy and manage a pod based on that image.

### Steps (CLI)

1. $ `crc console`
1. $ `eval $(crc oc-env)`
1. $ `oc login -u developer -p developer https://api.crc.testing:6443`
1. $ `oc get projects`
1. $ `oc new-project demo-31`
1. $ `oc new-app sonatype/nexus:oss`
1. $ `oc expose service/nexus`
1. $ `oc get all`
1. $ `oc get is`
1. $ `oc describe is/nexus`
1. $ `oc describe pods`
1. $ `oc get pods -o wide`
1. $ `oc explain pods`
1. $ `BROWSE As per Your URL : http://nexus-demo-31.apps-crc.testing/nexus/
1. $ `oc delete all --selector app=nexus`
1. $ `oc help`
1. $ `oc create --help` 

### Steps (Web Console)

https://redhatgov.io/workshops/openshift_4_101/lab2-byocontainer/

# Summary

In this lab, you pulled an example container image down from [Quay.io](https://quay.io/), and deployed it into a pod running in OpenShift. You exposed a route for clients to access that service via their web browsers. And you learned how to get and describe resources using both the command line and the web console. Hopefully, this lab also helped to get you familiar with using the CLI and navigating within the web console.

# Additional resources:

[Level Up video: "CodeReady Containers Quick Intro"](https://youtu.be/bD7R0n_LyGo)

# [Module 01 <<](../Module%2001%20-%20Overview) | [>> NEXT: Module 03 - Deploying Via S2I](../Module%2003%20-%20Deploying%20via%20S2I)
