# Istio and Red Hat OpenShift on IBM Cloud
[Istio](https://www.ibm.com/cloud/info/istio) is an open platform to connect, secure, control and observe microservices, also known as a service mesh, on cloud platforms such as Kubernetes in OpenShift. With Istio, you can manage network traffic, load balance across microservices, enforce access policies, verify service identity, secure service communication and observe what exactly is going on with your services.

![Istio Service Mesh Explained](http://img.youtube.com/vi/6zDrLvpfCK4/0.jpg)

![https://youtu.be/6zDrLvpfCK4](https://youtu.be/6zDrLvpfCK4)

Based on the open source Istio project, Red Hat OpenShift Service Mesh adds a transparent layer on existing distributed applications. Red Hat OpenShift Service Mesh provides a platform for behavioral insight and operational control over your networked microservices in a service mesh. With Red Hat OpenShift Service Mesh, you can connect, secure, and monitor microservices in your OpenShift Container Platform environment.

In this course, you can see how to install Service Mesh alongside microservices for a simple mock app called [Guestbook](https://github.com/IBM/guestbook). 

## Objectives
After you complete this course, you'll be able to:
- Install Red Hat OpenShift Service Mesh in your cluster
- Deploy the Guestbook sample app
- Use metrics, logging and tracing to observe services
- Set up the Istio Ingress Gateway
- Perform simple traffic management, such as A/B tests and canary deployments
- Secure your mesh using mTLS

## Architecture
![](README_images/istio-openshift.png)

## Workshop setup
* [Access your cluster](exercise-1/README.md)
* [Installing Service Mesh](exercise-2/README.md)

## Deploy Sample
* [Deploy Guestbook app](exercise-3/README.md)
* [Expose the app using Ingress](exercise-4/README.md)

## Use Istio
* [Observability](exercise-5/README.md)
* [Perform traffic management](exercise-6/README.md)
* [Secure your mesh](exercise-7/README.md)