# Exercise 2 - Installing Istio on Red Hat OpenShift


## Install the Operators
To install the Red Hat OpenShift Service Mesh Operator, you must first install Elasticsearch, Jaeger, and Kiali Operators.
![](assets/../../assets/installed-opertors.png)
  
1. From the **OpenShift web console**, select **Administrator** in the drop down
2. Then select **Operators** -> **OperatorHub**
3. Search for **Elasticsearch Operator** -> **Install** -> **Subscribe**
4. **OperatorHub** -> **Red Hat OpenShift Jaeger ** -> **Install** -> **Subscribe**
5. **OperatorHub** -> **Kiali Operator** -> **Install** -> **Subscribe**
6. **OperatorHub** -> **Red Hat OpenShift Service Mesh** -> **Install** -> **Subscribe**


## Deploying the Red Hat OpenShift Service Mesh control plane

The operator uses a `ServiceMeshControlPlane` resource to determine how to install Istio and what components you want. Let's create that resource now.

1.  Create a new project by going to **Home** -> **Projects** -> **Create Project**
2.  Enter `istio-system` in the **Name** and click **Create**
3.  Navigate to **Operators** -> **Installed Operators**
4.  Click the **Red Hat OpenShift Service Mesh Operator**. If you don't see it, wait a couple of minutes and refresh.
5.  Under **Istio Service Mesh Control Plane** click **Create ServiceMeshControlPlane**.
6.  Then, click **Create**. The Operator creates Pods, services, and Service Mesh control plane components based on your configuration parameters.

### Create a ServiceMeshMemberRoll
ServiceMeshMemberRoll resource is used to to specify the namespaces associated with the Service Mesh.

![](assets/../../assets/servicemeshmemberroll.png)

1. Navigate to **Operators** → **Installed Operators** again.
2. Click the **Red Hat OpenShift Service Mesh Operator**.
3. In the tab area, scroll to the right to find **Istio Service Mesh Member Roll** 
4. Click **Create ServiceMeshMemberRoll**
5. Change `your-project` to `bookinfo` and delete the last line.
6. Then, click **Create**. 
    
Congratulations! You successfully installed Istio into your cluster and configured the `bookinfo` project to use it.


#### [Continue to Exercise 3 - BookInfo](../exercise-3/README.md)
