# Exercise 3 - Deploy the BookInfo app in to the mesh

The BookInfo app is a sample app for users to leave comments. It consists of a web front end, Redis master for storage, and a replicated set of Redis slaves. We will also integrate the app with Watson Tone Analyzer which detects the sentiment in users' comments and replies with emoticons.

![](../README_images/withistio.svg)



## Clone application source repo

```shell
git clone https://github.com/rvennam/istio-roks-101
cd istio-roks-101/bookinfo
```

## Install the BookInfo app

1.  From your **IBM Cloud Shell** create a project called "bookinfo"
    ``` shell
    oc new-project bookinfo
    ```
    
1. Inject the Istio Envoy sidecar into the bookinfo pods, and deploy the BookInfo app on to the Kubernetes cluster. Deploy both the v1 and v2 versions of the app:

    ```shell
    oc apply -f bookinfo.yaml
    ```

These commands deploy the BookInfo app on to the cluster. Since we enabled automation sidecar injection, these pods will be also include an Envoy sidecar as they are started in the cluster. Here we have two versions of deployments, a new version (`v2`) in the current directory, and a previous version (`v1`) in a sibling directory. They will be used in future sections to showcase the Istio traffic routing capabilities.

1. Verify that the pods are up and running.

    ```shell
    oc get pods
    ```
    Sample output:
    ```shell
    NAME                              READY     STATUS    RESTARTS   AGE
    details-v1-789c5f58f4-9twtw       2/2       Running   0          4m12s
    productpage-v1-856c8cc5d8-xcx2q   2/2       Running   0          4m11s
    ratings-v1-5786768978-tr8z9       2/2       Running   0          4m12s
    reviews-v1-5874566865-mxfgm       2/2       Running   0          4m12s
    reviews-v2-86865fc7d9-mf6t4       2/2       Running   0          4m12s
    reviews-v3-8d4cbbbbf-rfjcz        2/2       Running   0          4m12s
    ```

    Note that each bookinfo pods has 2 containers in it. One is the bookinfo container, and the other is the Envoy proxy sidecar.

Your bookinfo app is running, but you can't access it! In the next exercise you will expose the productpage service to allow incoming traffic.

#### [Continue to Exercise 4 - Ingress Gateway](../exercise-4/README.md)
