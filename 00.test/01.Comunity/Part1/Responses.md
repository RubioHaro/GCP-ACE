1.Every employee of your company has a Google account. Your operational team needs to manage a large number of instances on Compute Engine. Each member of this team needs only administrative access to the servers. Your security team wants to ensure that the deployment of credentials is operationally efficient and must be able to determine who accessed a given instance. What should you do?


    R: C. Ask each member of the team to generate a new SSH key pair and to add the public key to their Google account. Grant the compute.osAdminLogin role to the Google group corresponding to this team. 


Feedback: 

    R: C is correct, the others either involve too much effort or are insecure, and sharing a key pair means you can't distinguish its users anymore.

2.You need to create a custom VPC with a single subnet. The subnet's range must be as large as possible. Which range should you use?

    R: B.

Feedback: 

    Therefore, although the IP address 0.0.0.0/0 represents the entire Internet, it is not a routable IP address itself since it cannot be assigned to a specific device. Then, the answer is B, the second large range of ip addresses.

3.You want to select and configure a cost-effective solution for relational data on Google Cloud Platform. You are working with a small set of operational data in one geographic location. You need to support point-in-time recovery. What should you do?

    R: A. Select Cloud SQL (MySQL). Verify that the enable binary logging option is selected.

Feedback:

    Reference https://cloud.google.com/sql/docs/mysql/backup-recovery/restore


4.You want to configure autohealing for network load balancing for a group of Compute Engine instances that run in multiple zones, using the fewest possible steps.
You need to configure re-creation of VMs if they are unresponsive after 3 attempts of 10 seconds each. What should you do?

    R: C. Create a managed instance group. Set the Autohealing health check to healthy (HTTP) 

Feedback:

    A.B.D all don't enable Autohealing to recreate unresponsive VMs, so answer should be C.

5.You are using multiple configurations for gcloud. You want to review the configured Kubernetes Engine cluster of an inactive configuration using the fewest possible steps. What should you do?

Extra: The gcloud config command group lets you set, view and unset properties used by Google Cloud CLI.

    R: D. Use kubectl config use-context and kubectl config view to review the output. 

Feedback:

    Kubectl with Kubernetes Engine leverages Google Cloud Platform’s gcloud CLI to facilitate auth against clusters.
    Reference https://medium.com/google-cloud/kubernetes-engine-kubectl-config-b6270d2b656c

6.Your company uses Cloud Storage to store application backup files for disaster recovery purposes. You want to follow Google's recommended practices. Which storage option should you use?

    R: Coldline Storage, because it is the most cost-effective option.

Feedback:

    The correct answer would depend on the specific requirements of the backup files. So, try to follow the next considerations:
    If the backup files need to be accessed infrequently and data retrieval within several hours or days is acceptable, then Coldline Storage would be the most cost-effective option.
    If the backup files need to be accessed within seconds and the cost is not a concern, then Nearline Storage would be a suitable option.
    If the backup files need to be accessible at all times and the cost is not a concern, then Multi-Regional Storage would be the best option as it provides high durability and availability, as well as low latency access to your data.
    It is important to consider the specific requirements of your backup files and choose the storage option that best meets those needs.

7.Several employees at your company have been creating projects with Cloud Platform and paying for it with their personal credit cards, which the company reimburses. The company wants to centralize all these projects under a single, new billing account. What should you do?


    R: C, In the Google Platform Console, go to the Resource Manage and move all projects to the root Organizarion. Then, create a new billing account and set up a payment method and change the billing account of each project.

Feedback:
    
    A is incorrect, as a good practice, you should not use share your bank account information. Google never asks for your bank account information. You can contact Google to request a partner manager to help you with the billing process.
    B is incorrect Google will never ask you to send them your credit card information. As the previous answer, you can contact Google to request a partner manager to help you with the billing process.
    C is correct, you can move all projects to the root organization and then create a new billing account and set up a payment method. 
    D because only the creation of a new billing account is not enough, you need to change the billing account of each project.

8.You have an application that looks for its licensing server on the IP 10.0.3.21. You need to deploy the licensing server on Compute Engine. You do not want to change the configuration of the application and want the application to be able to reach the licensing server. What should you do?

    R: Reserve the IP 10.0.3.21 as a static internal IP address using gcloud and assign it to the licensing server.

Feedback:

    Note the internal IP address of the licensing server. Reserve the IP as a static internal IP address using gcloud and assign it to the licensing server. This way, the application will be able to reach the licensing server.

9.You are deploying an application to App Engine. You want the number of instances to scale based on request rate. You need at least 3 unoccupied instances at all times. Which scaling type should you use?
    
    R: Automatic Scaling with min_idle_instances set to 3.

Feedback:

    Automatic scaling creates instances based on request rate, response latencies, and other application metrics. You can specify thresholds for each of these metrics, as well as a minimum number instances to keep running at all times.

10.You have a development project with appropriate IAM roles defined. You are creating a production project and want to have the same IAM roles on the new project, using the fewest possible steps. What should you do?

    R: A, Use gcloud iam roles copy and specify the production project as the destination project.

Feedback:

    A is correct, you can use gcloud iam roles copy to copy the roles from the development project to the production project.
    B is incorrect, because we want to copy the roles from the development project to the production project, not to the organization.
    C, D are incorrect, because don't copy the roles from the development project to the production project. 

11.You need a dynamic way of provisioning VMs on Compute Engine. The exact specifications will be in a dedicated configuration file. You want to follow Google's recommended practices. Which method should you use?

    R: A, Deployment Manager

Feedback:

    Deployment Manager is a configuration management tool that allows you to define and deploy a set of resources, including Compute Engine VMs, in a declarative manner.

12.You have a Dockerfile that you need to deploy on Kubernetes Engine. What should you do?


    R: C, Create a docker image from the Dockerfile and upload it to Container Registry. Create a Deployment YAML file to point to that image. Use kubectl to create the deployment with that file. 

Feedback:

    The correct answer is Option C. To deploy a Docker container on Kubernetes Engine, you should first create a Docker image from the Dockerfile and push it to Container Registry, which is a fully-managed Docker container registry that makes it easy for you to store, manage, and deploy Docker container images. Then, you can create a Deployment YAML file that specifies the image to use and other desired deployment options, and use the kubectl command-line tool to create the deployment based on the YAML file.

    Option A is incorrect because kubectl app deploy is not a valid command.

    Option B is incorrect because gcloud app deploy is used to deploy applications to App Engine, not Kubernetes Engine.

    Option D is incorrect because it involves storing the image in Cloud Storage rather than Container Registry.

13.Your development team needs a new Jenkins server for their project. You need to deploy the server using the fewest steps possible. What should you do?

    R: Use GCP Marketplace to launch the Jenkins solution.

Feedback:

    GCP Marketplace is a curated catalog of enterprise solutions that run on Google Cloud Platform. You can deploy these solutions with a few clicks, and they are fully supported by Google.

14.You need to update a deployment in Deployment Manager without any resource downtime in the deployment. Which command should you use?

    R: B. gcloud deployment-manager deployments update --config <deployment-config-path>

Feedback:

    Update and create resource is not even a command under deployment management service.

15.You need to run an important query in BigQuery but expect it to return a lot of records. You want to find out how much it will cost to run the query. You are using on-demand pricing. What should you do?

    R: B, Use the command line to run a dry run query to estimate the number of bytes read. Then convert that bytes estimate to dollars using the Pricing Calculator.

Feedback:

    Under on-demand pricing, BigQuery charges for queries by using one metric: the number of bytes processed (also referred to as bytes read). You are charged for the number of bytes processed whether the data is stored in BigQuery or in an external data source such as Cloud Storage, Drive, or Cloud Bigtable. On-demand pricing is based solely on usage.

