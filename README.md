![kubernetes-horizontal-color](https://github.com/refanarasheed/21312045-isec6000-assignment1-task1/assets/143176582/d89b9c37-afc8-4b40-997b-ddf2478eba96)

<div align="center">image courtesy: Kubernetes</div>

# Create Kubernetes Cluster on Google Kubernetes Engine
1)	Access the Google Cloud Console by signing in
2)	Follow the steps below to **create a new project**:
       1) In the Google Cloud console, go to the Manage Resources page. Here is a link that you can use for easy access: [Go to Manage Resources](https://console.cloud.google.com/cloud-resource-manager?walkthrough_id=resource-manager--create-project&start_index=1&_ga=2.210894805.1333585992.1693288858-1368561227.1693027365&_gac=1.54144346.1693027503.CjwKCAjwoqGnBhAcEiwAwK-OkdDkdFh8ORWsvhT0rYfi1Z1M_rtcCVCt1oi9nYEgsSw0TueDC7ddFhoCx90QAvD_BwE#step_index=1)
       3) Then click the **Create Project** button
          ![image13](https://github.com/refanarasheed/21312045-isec6000-assignment1-task1/assets/143176582/dbbb476b-6092-4be6-812e-3eee969a6d4c)

       4) Create a new project named '**21312045-ISEC6000-Task1**' in the New Project window. A project name must be between 4 and 30 characters long and can only contain letters, numbers, single quotes, hyphens,spaces, or exclamation points.
       5) In the Location box, enter the parent organization or folder resource. That resource will serve as the new project's hierarchical parent. If there is no option for an organization, you can use it to create your new project as the top level of its own resource hierarchy.
       6) When you are finished entering new project information, click **Create**
          ![image25](https://github.com/refanarasheed/21312045-isec6000-assignment1-task1/assets/143176582/a9e583ad-2189-44c2-b567-c19506a5d4e3)

       7) Activate the Google Kubernetes Engine and Artifact Registry APIs by clicking the link: [Enable the APIs](https://console.cloud.google.com/flows/enableapiapiid=artifactregistry.googleapis.com,container.googleapis.com)

       8) To launch the cloud shell, click the **Activate Cloud Shell** button, which is located next to the search toolbar in the upper-right corner of the console. Cloud Shell gives you command-line access to Google Cloud computing resources. Cloud Shell includes the Google Cloud CLI and the kubectl command-line tool. The gcloud CLI is the primary command-line interface for Google Cloud, while kubectl is the primary command-line interface for running commands against Kubernetes clusters. 
          A Cloud Shell session appears in a frame lower on the console.
          ![image18](https://github.com/refanarasheed/21312045-isec6000-assignment1-task1/assets/143176582/a1ea6bc5-b4bb-473a-9b72-4a0f2238f40d)

          This shell is used to execute gcloud and kubectl commands. Set your default project in the Google Cloud CLI by running the below command:
          ```
          gcloud config set project isec6000-task1 
          ```
          You can then **authorize Cloud Shell** if this is your first time using it
          ![image26](https://github.com/refanarasheed/21312045-isec6000-assignment1-task1/assets/143176582/022a3d54-dc4c-4fae-ba88-d61299b24f97)

          Choose a Default Compute Zone: The Compute Zone aids in providing a general idea of where the clusters and resources will be located physically.
          Run the following command in the cloud shell to set your default compute zone:
          ```
          cloud config set compute/zone us-central1-a 
          ```
          Note: You can change us-central1-a to any zone you want.
          ![image34](https://github.com/refanarasheed/21312045-isec6000-assignment1-task1/assets/143176582/34d0d54d-3300-4dd6-91b5-e16c83c1e0f7)

3)  Now, from the navigation menu, select Kubernetes Engine, followed by **Clusters**

4) Configure your cluster's settings, such as the name, location, and node pool configuration. Then click **Create** to provision your GKE cluster.
    ![image31](https://github.com/refanarasheed/21312045-isec6000-assignment1-task1/assets/143176582/8668d953-7ac5-4686-beb0-c2547959724e)

    The cluster '**isec6000-cluster-task1**' is created now
    ![image9](https://github.com/refanarasheed/21312045-isec6000-assignment1-task1/assets/143176582/fb77e895-cb56-4912-b0a3-65ac120ec8af)

# Install and configure kubectl to manage your Kubernetes cluster
1) After creating the GKE cluster, click on the **connect** listed in the cluster action
   ![image16](https://github.com/refanarasheed/21312045-isec6000-assignment1-task1/assets/143176582/019a1db1-c84e-4952-98d9-5d466e97edc8)

2) A dialog box will pop up, now click on the **run in cloud** shell button to configure Kubectl command line access
  ![image12](https://github.com/refanarasheed/21312045-isec6000-assignment1-task1/assets/143176582/a588aa59-744f-4286-bf48-310cca3b0860)
