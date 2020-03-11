# Exercise 2 - Installing Istio on IBM Cloud Kubernetes Service


## Install the Operator
  
1.  Navigate to your cluster in the [IBM Cloud Dashboard](https://cloud.ibm.com/kubernetes/clusters)

2. Click on your cluster

3. Launch OpenShift web console

4. Select **Administrator** in the drop down and then select **Operators** -> **OperatorHub**

5. Search for *Service Mesh* and select **Red Hat OpenShift Service Mesh**

6. Click **Install** and then **Subscribe**

7. Click on **Installed Operators** and refresh the page to see the changes.


## Deploying the Red Hat OpenShift Service Mesh control plane

1.  Create a new project by going to **Home** -> **Projects** -> **Create Project**
2.  Enter `istio-system` in the **Name** and click **Create**
3.  Navigate to **Operators** -> **Installed Operators**
4.  Click the **Red Hat OpenShift Service Mesh Operator**. 
5.  Under **Istio Service Mesh Control Plane** click **Create Instance**.
6.  Then, click **Create**. The Operator creates Pods, services, and Service Mesh control plane components based on your configuration parameters.
7.  Navigate to **Operators** → **Installed Operators** again.
8.  Click the **Red Hat OpenShift Service Mesh Operator**.
9.  Under **Istio Service Mesh Member Roll** click **Create Instance**
10. Change `your-project` to `guestbook` and delete the last line
11. Then, click **Create**. 
    
Congratulations! You successfully installed Istio into your cluster and configured the `guestbook` project to use it.
