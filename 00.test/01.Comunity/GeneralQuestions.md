# Cloud Engineer: Community Questions

Las siguientes preguntas de ejemplo le ayudarán a familiarizarse con el formato de las preguntas del examen y con el contenido que pudiera cubrir el examen.

## Preguntas: 

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



16.You have a single binary application that you want to run on Google Cloud Platform. You decided to automatically scale the application based on underlying infrastructure CPU usage. Your organizational policies require you to use virtual machines directly. You need to ensure that the application scaling is operationally efficient and completed as quickly as possible. What should you do?


Create a Google Kubernetes Engine cluster, and use horizontal pod autoscaling to scale the application.
Create an instance template, and use the template in a managed instance group with autoscaling configured.
Create an instance template, and use the template in a managed instance group that scales up and down based on the time of day.
Use a set of third-party tools to build automation around scaling the application up and down, based on Stackdriver CPU usage monitoring.

    B

17.You are analyzing Google Cloud Platform service costs from three separate projects. You want to use this information to create service cost estimates by service type, daily and monthly, for the next six months using standard query syntax. What should you do?
A. Export your bill to a Cloud Storage bucket, and then import into Cloud Bigtable for analysis.
B. Export your bill to a Cloud Storage bucket, and then import into Google Sheets for analysis.
C. Export your transactions to a local file, and perform analysis with a desktop tool.
D. Export your bill to a BigQuery dataset, and then write time window-based SQL queries for analysis.

    D.

18.You need to set up a policy so that videos stored in a specific Cloud Storage Regional bucket are moved to Coldline after 90 days, and then deleted after one year from their creation. How should you set up the policy?
A. Use Cloud Storage Object Lifecycle Management using Age conditions with SetStorageClass and Delete actions. Set the SetStorageClass action to 90 days and the Delete action to 275 days (365 ג€" 90)
B. Use Cloud Storage Object Lifecycle Management using Age conditions with SetStorageClass and Delete actions. Set the SetStorageClass action to 90 days and the Delete action to 365 days.
C. Use gsutil rewrite and set the Delete action to 275 days (365-90).
D. Use gsutil rewrite and set the Delete action to 365 days.


    B (FEEEDBACK)

19.You have a Linux VM that must connect to Cloud SQL. You created a service account with the appropriate access rights. You want to make sure that the VM uses this service account instead of the default Compute Engine service account. What should you do?

A. When creating the VM via the web console, specify the service account under the 'Identity and API Access' section. Most Voted
B. Download a JSON Private Key for the service account. On the Project Metadata, add that JSON as the value for the key compute-engine-service- account.
C. Download a JSON Private Key for the service account. On the Custom Metadata of the VM, add that JSON as the value for the key compute-engine- service-account. Most Voted
D. Download a JSON Private Key for the service account. After creating the VM, ssh into the VM and save the JSON under ~/.gcloud/compute-engine-service- account.json.

21.You have one GCP account running in your default region and zone and another account running in a non-default region and zone. You want to start a new
Compute Engine instance in these two Google Cloud Platform accounts using the command line interface. What should you do?
A. Create two configurations using gcloud config configurations create [NAME]. Run gcloud config configurations activate [NAME] to switch between accounts when running the commands to start the Compute Engine instances. Most Voted
B. Create two configurations using gcloud config configurations create [NAME]. Run gcloud configurations list to start the Compute Engine instances.
C. Activate two configurations using gcloud configurations activate [NAME]. Run gcloud config list to start the Compute Engine instances.
D. Activate two configurations using gcloud configurations activate [NAME]. Run gcloud configurations list to start the Compute Engine instances.

    A. Create two configurations using gcloud config configurations create [NAME]. Run gcloud config configurations activate [NAME] to switch between accounts when running the commands to start the Compute Engine instances. Most Voted


22.You significantly changed a complex Deployment Manager template and want to confirm that the dependencies of all defined resources are properly met before committing it to the project. You want the most rapid feedback on your changes. What should you do?
A. Use granular logging statements within a Deployment Manager template authored in Python.
B. Monitor activity of the Deployment Manager execution on the Stackdriver Logging page of the GCP Console.
C. Execute the Deployment Manager template against a separate project with the same configuration, and monitor for failures.
D. Execute the Deployment Manager template using the ג€"-preview option in the same project, and observe the state of interdependent resources.

    D. feedback

23.You are building a pipeline to process time-series data. Which Google Cloud Platform services should you put in boxes 1,2,3, and 4?

![](IMG1.jpg)

A. Cloud Pub/Sub, Cloud Dataflow, Cloud Datastore, BigQuery
B. Firebase Messages, Cloud Pub/Sub, Cloud Spanner, BigQuery
C. Cloud Pub/Sub, Cloud Storage, BigQuery, Cloud Bigtable
D. Cloud Pub/Sub, Cloud Dataflow, Cloud Bigtable, BigQuery

The correct process for building a pipeline to process time-series data. Here's how each of the components is used:

1. Cloud Pub/Sub: receives and distributes time-series data from different sources.
2. Cloud Dataflow: processes the data by applying transformations and analytics.
3. Cloud Bigtable: stores and manages the processed data as a NoSQL database.
4. BigQuery: provides a SQL-like interface to analyze the data and extract insights.

By combining these components, you can create a scalable and reliable pipeline to process and analyze time-series data in real time.

24.You have a project for your App Engine application that serves a development environment. The required testing has succeeded and you want to create a new project to serve as your production environment. What should you do?

A. Use gcloud to create the new project, and then deploy your application to the new project.
B. Use gcloud to create the new project and to copy the deployed application to the new project.
C. Create a Deployment Manager configuration file that copies the current App Engine deployment into a new project.
D. Deploy your application again using gcloud and specify the project parameter with the new project name to create the new project.

    A. Use gcloud to create the new project, and then deploy your application to the new project.


25.You need to configure IAM access audit logging in BigQuery for external auditors. You want to follow Google-recommended practices. What should you do?
A. Add the auditors group to the 'logging.viewer' and 'bigQuery.dataViewer' predefined IAM roles. Most Voted
B. Add the auditors group to two new custom IAM roles.
C. Add the auditor user accounts to the 'logging.viewer' and 'bigQuery.dataViewer' predefined IAM roles.
D. Add the auditor user accounts to two new custom IAM roles.

26.You need to set up permissions for a set of Compute Engine instances to enable them to write data into a particular Cloud Storage bucket. You want to follow Google-recommended practices. What should you do?

A. Create a service account with an access scope. Use the access scope 'https://www.googleapis.com/auth/devstorage.write_only'.
B. Create a service account with an access scope. Use the access scope 'https://www.googleapis.com/auth/cloud-platform'.
C. Create a service account and add it to the IAM role 'storage.objectCreator' for that bucket.*
D. Create a service account and add it to the IAM role 'storage.objectAdmin' for that bucket.

    B. Create a service account with an access scope. Use the access scope 'https://www.googleapis.com/auth/cloud-platform'.
 
30.You are creating a Google Kubernetes Engine (GKE) cluster with a cluster autoscaler feature enabled. You need to make sure that each node of the cluster will run a monitoring pod that sends container metrics to a third-party monitoring solution. What should you do?

    B. Deploy the monitoring pod as a DeamonSet. The DaemonSet will ensure that a monitoring pod is running on each node of the cluster.

You want to send and consume Cloud Pub/Sub messages from your App Engine application. The Cloud Pub/Sub API is currently disabled. You will use a service account to authenticate your application to the API. You want to make sure your application can use Cloud Pub/Sub. What should you do?

    A. Enable the Cloud Pub/Sub API in the API Library on the GCP Console.

You need to monitor resources that are distributed over different projects in Google Cloud Platform. You want to consolidate reporting under the same Stackdriver
Monitoring dashboard. What should you do?

    C. Configure a single StackDriver Account and link all the projects to it.

33.You are deploying an application to a Compute Engine VM in a managed instance group. The application must be running at all times, but only a single instance of the VM should run per GCP project. How should you configure the instance group?

    A. Set autoescaling to ON, set the minimum number of instances to 1, and set the maximum number of instances to 1.

36.You have one project called proj-sa where you manage all your service accounts. You want to be able to use a service account from this project to take snapshots of VMs running in another project called proj-vm. What should you do?

    C, Grant the service account the IAM Role of Compute Storage Admin on the project where the VMs are running.

37.You created a Google Cloud Platform project with an App Engine application inside the project. You initially configured the application to be served from the us- central region. Now you want the application to be served from the asia-northeast1 region. What should you do?


    D. Create a new GCP project and create an App Engine application inside this new project. Specify asia-northeast1 as the region to serve your application. Most Voted

39.You create a new Google Kubernetes Engine (GKE) cluster and want to make sure that it always runs a supported and stable version of Kubernetes. What should you do?


    B. Enable the Node Auto-Upgrades feature for your GKE cluster. Most Voted

40.You have an instance group that you want to load balance. You want the load balancer to terminate the client SSL session. The instance group is used to serve a public web application over HTTPS. You want to follow Google-recommended practices. What should you do?

    A. Configure an HTTP(S) load balancer. Most Voted

41.You have 32 GB of data in a single file that you need to upload to a Nearline Storage bucket. The WAN connection you are using is rated at 1 Gbps, and you are the only one on the connection. You want to use as much of the rated 1 Gbps as possible to transfer the file rapidly. How should you upload the file?


    B. Enable parallel composite uploads using gsutil on the file transfer. Most Voted

43.You are running an application on multiple virtual machines within a managed instance group and have autoscaling enabled. The autoscaling policy is configured so that additional instances are added to the group if the CPU utilization of instances goes above 80%. VMs are added until the instance group reaches its maximum limit of five VMs or until CPU utilization of instances lowers to 80%. The initial delay for HTTP health checks against the instances is set to 30 seconds.
The virtual machine instances take around three minutes to become available for users. You observe that when the instance group autoscales, it adds more instances then necessary to support the levels of end-user traffic. You want to properly maintain instance group sizes when autoscaling. What should you do?


    D. Increase the initial delay of the HTTP health check to 200 seconds. Most Voted

44.You need to select and configure compute resources for a set of batch processing jobs. These jobs take around 2 hours to complete and are run nightly. You want to minimize service costs. What should you do?


    C. Select Compute Engine. Use preemptible VM instances of the appropriate standard machine type. Most Voted

45.You recently deployed a new version of an application to App Engine and then discovered a bug in the release. You need to immediately revert to the prior version of the application. What should you do?


    C. On the App Engine Versions page of the GCP Console, route 100% of the traffic to the previous version. Most Voted

46.You deployed an App Engine application using gcloud app deploy, but it did not deploy to the intended project. You want to find out why this happened and where the application deployed. What should you do?


    D. Go to Cloud Shell and run gcloud config list to review the Google Cloud configuration used for deployment. Most Voted

47.You want to configure 10 Compute Engine instances for availability when maintenance occurs. Your requirements state that these instances should attempt to automatically restart if they crash. Also, the instances should be highly available including during system maintenance. What should you do?


    A. Create an instance template for the instances. Set the 'Automatic Restart' to on. Set the 'On-host maintenance' to Migrate VM instance. Add the instance template to an instance group. Most Voted

48.You host a static website on Cloud Storage. Recently, you began to include links to PDF files on this site. Currently, when users click on the links to these PDF files, their browsers prompt them to save the file onto their local system. Instead, you want the clicked PDF files to be displayed within the browser window directly, without prompting the user to save the file locally. What should you do?


    C. Set Content-Type metadata to application/pdf on the PDF file objects. Most Voted

49.You have a virtual machine that is currently configured with 2 vCPUs and 4 GB of memory. It is running out of memory. You want to upgrade the virtual machine to have 8 GB of memory. What should you do?

    D. Stop the VM, increase the memory to 8 GB, and start the VM. Most Voted

50.You have production and test workloads that you want to deploy on Compute Engine. Production VMs need to be in a different subnet than the test VMs. All the
VMs must be able to reach each other over Internal IP without creating additional routes. You need to set up VPC and the 2 subnets. Which configuration meets these requirements?


    A. Create a single custom VPC with 2 subnets. Create each subnet in a different region and with a different CIDR range. Most Voted

51.You need to create an autoscaling managed instance group for an HTTPS web application. You want to make sure that unhealthy VMs are recreated. What should you do?

    A. Create a health check on port 443 and use that when creating the Managed Instance Group. Most Voted

54.You are given a project with a single Virtual Private Cloud (VPC) and a single subnetwork in the us-central1 region. There is a Compute Engine instance hosting an application in this subnetwork. You need to deploy a new instance in the same project in the europe-west1 region. This new instance needs access to the application. You want to follow Google-recommended practices. What should you do?


    A. 1. Create a subnetwork in the same VPC, in europe-west1. 2. Create the new instance in the new subnetwork and use the first instance's private address as the endpoint. Most Voted

55.Your projects incurred more costs than you expected last month. Your research reveals that a development GKE container emitted a huge number of logs, which resulted in higher costs. You want to disable the logs quickly using the minimum number of steps. What should you do?

    A. 1. Go to the Logs ingestion window in Stackdriver Logging, and disable the log source for the GKE container resource. Most Voted


57.You have a web application deployed as a managed instance group. You have a new version of the application to gradually deploy. Your web application is currently receiving live web traffic. You want to ensure that the available capacity does not decrease during the deployment. What should you do?


    B.Perform a rolling-action start-update with maxSurge set to 1 and maxUnavailable set to 0. 

58.You are building an application that stores relational data from users. Users across the globe will use this application. Your CTO is concerned about the scaling requirements because the size of the user base is unknown. You need to implement a database solution that can scale with your user growth with minimum configuration changes. Which storage solution should you use?


    B. Cloud Spanner, is a distributed SQL database management and storage servide, provides automaric multi-site replication and failover.
Base de datos relacional, diseñada para escalarse

61.Your organization is a financial company that needs to store audit log files for 3 years. Your organization has hundreds of Google Cloud projects. You need to implement a cost-effective approach for log file retention. What should you do?

    B. Create an export to the sink that saves logs from Cloud Audit to a Coldline Storage bucket. Most Voted


62.You want to run a single caching HTTP reverse proxy on GCP for a latency-sensitive website. This specific reverse proxy consumes almost no CPU. You want to have a 30-GB in-memory cache, and need an additional 2 GB of memory for the rest of the processes. You want to minimize cost. How should you run this reverse proxy?

    A. Create a Cloud Memorystore for Redis instance with 32-GB capacity. Most Voted

63.You are hosting an application on bare-metal servers in your own data center. The application needs access to Cloud Storage. However, security policies prevent the servers hosting the application from having public IP addresses or access to the internet. You want to follow Google-recommended practices to provide the application with access to Cloud Storage. What should you do?

    D. 1. Using Cloud VPN or Interconnect, create a tunnel to a VPC in Google Cloud. 2. Use Cloud Router to create a custom route advertisement for 199.36.153.4/30. Announce that network to your on-premises network through the VPN tunnel. 3. In your on-premises network, configure your DNS server to resolve *.googleapis.com as a CNAME to restricted.googleapis.com. Most Voted

64.You want to deploy an application on Cloud Run that processes messages from a Cloud Pub/Sub topic. You want to follow Google-recommended practices. What should you do?

    C. 1. Create a service account. 2. Give the Cloud Run Invoker role to that service account for your Cloud Run application. 3. Create a Cloud Pub/Sub subscription that uses that service account and uses your Cloud Run application as the push endpoint. Most Voted

65.You need to deploy an application, which is packaged in a container image, in a new project. The application exposes an HTTP endpoint and receives very few requests per day. You want to minimize costs. What should you do?

    B. Deploy the container on Cloud Run on GKE.

38.For analysis purposes, you need to send all the logs from all of your Compute Engine instances to a BigQuery dataset called platform-logs. You have already installed the Cloud Logging agent on all the instances. You want to minimize cost. What should you do?


    C. 1. In Cloud Logging, create a filter to view only Compute Engine logs. 2. Click Create Export. 3. Choose BigQuery as Sink Service, and the platform-logs dataset as Sink Destination. Most Voted


69.You are using Deployment Manager to create a Google Kubernetes Engine cluster. Using the same Deployment Manager deployment, you also want to create a
DaemonSet in the kube-system namespace of the cluster. You want a solution that uses the fewest possible services. What should you do?

    A. Add the cluster's API as a new Type Provider in Deployment Manager, and use the new type to create the DaemonSet. Most Voted

70.You are building an application that will run in your data center. The application will use Google Cloud Platform (GCP) services like AutoML. You created a service account that has appropriate access to AutoML. You need to enable authentication to the APIs from your on-premises environment. What should you do?

    B. Use gcloud to create a key file for the service account that has appropriate permissions. Most Voted

71.You are using Container Registry to centrally store your company's container images in a separate project. In another project, you want to create a Google
Kubernetes Engine (GKE) cluster. You want to ensure that Kubernetes can download images from Container Registry. What should you do?


    A. In the project where the images are stored, grant the Storage Object Viewer IAM role to the service account used by the Kubernetes nodes. Most Voted

72.You deployed a new application inside your Google Kubernetes Engine cluster using the YAML file specified below.
You check the status of the deployed pods and notice that one of them is still in PENDING status:

    C. Review details of myapp-deployment-58ddbbb995-lp86m Pod and check for warning messages. Most Voted

73.You are setting up a Windows VM on Compute Engine and want to make sure you can log in to the VM via RDP. What should you do?

    B. After the VM has been created, use gcloud compute reset-windows-password to retrieve the login credentials for the VM. Most Voted

74.You want to configure an SSH connection to a single Compute Engine instance for users in the dev1 group. This instance is the only resource in this particular
Google Cloud Platform project that the dev1 users should be able to connect to. What should you do?

    A. Set metadata to enable-oslogin=true for the instance. Grant the dev1 group the compute.osLogin role. Direct them to use the Cloud Shell to ssh to that instance. Most Voted

75.You need to produce a list of the enabled Google Cloud Platform APIs for a GCP project using the gcloud command line in the Cloud Shell. The project name is my-project. What should you do?

    A. Run gcloud projects list to get the project ID, and then run gcloud services list --project <project ID>.


77.You need to provide a cost estimate for a Kubernetes cluster using the GCP pricing calculator for Kubernetes. Your workload requires high IOPs, and you will also be using disk snapshots. You start by entering the number of nodes, average hours, and average days. What should you do next?

    A. Fill in local SSD. Fill in persistent disk storage and snapshot storage. Most Voted

78.You are using Google Kubernetes Engine with autoscaling enabled to host a new application. You want to expose this new application to the public, using HTTPS on a public IP address. What should you do?

    A. Create a Kubernetes Service of type NodePort for your application, and a Kubernetes Ingress to expose this Service via a Cloud Load Balancer. Most Voted

79.You need to enable traffic between multiple groups of Compute Engine instances that are currently running two different GCP projects. Each group of Compute
Engine instances is running in its own VPC. What should you do?


    B. Verify that both projects are in a GCP Organization. Share the VPC from one project and request that the Compute Engine instances in the other project use this shared VPC. Most Voted

81.You are operating a Google Kubernetes Engine (GKE) cluster for your company where different teams can run non-production workloads. Your Machine Learning
(ML) team needs access to Nvidia Tesla P100 GPUs to train their models. You want to minimize effort and cost. What should you do?

    D. Add a new, GPU-enabled, node pool to the GKE cluster. Ask your ML team to add the cloud.google.com/gke -accelerator: nvidia-tesla-p100 nodeSelector to their pod specification. Most Voted

85.You have a large 5-TB AVRO file stored in a Cloud Storage bucket. Your analysts are proficient only in SQL and need access to the data stored in this file. You want to find a cost-effective way to complete their request as soon as possible. What should you do?

    C. Create external tables in BigQuery that point to Cloud Storage buckets and run a SQL query on these external tables to complete your request. Most Voted

86.You need to verify that a Google Cloud Platform service account was created at a particular time. What should you do?

    A. Filter the Activity log to view the Configuration category. Filter the Resource type to Service Account. Most Voted

90.You want to configure a solution for archiving data in a Cloud Storage bucket. The solution must be cost-effective. Data with multiple versions should be archived after 30 days. Previous versions are accessed once a month for reporting. This archive data is also occasionally updated at month-end. What should you do?

    B. Add a bucket lifecycle rule that archives data with newer versions after 30 days to Nearline Storage. Most Voted

91.Your company's infrastructure is on-premises, but all machines are running at maximum capacity. You want to burst to Google Cloud. The workloads on Google
Cloud must be able to directly communicate to the workloads on-premises using a private IP range. What should you do?

    D. Set up Cloud VPN between the infrastructure on-premises and Google Cloud. Most Voted


92.You want to select and configure a solution for storing and archiving data on Google Cloud Platform. You need to support compliance objectives for data from one geographic location. This data is archived after 30 days and needs to be accessed annually. What should you do?

    D. Select Regional Storage. Add a bucket lifecycle rule that archives data after 30 days to Coldline Storage. Most Voted

93.Your company uses BigQuery for data warehousing. Over time, many different business units in your company have created 1000+ datasets across hundreds of projects. Your CIO wants you to examine all datasets to find tables that contain an employee_ssn column. You want to minimize effort in performing this task.
What should you do?

    A. Go to Data Catalog and search for employee_ssn in the search box. Most Voted
