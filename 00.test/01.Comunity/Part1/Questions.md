# Cloud Engineer: Community Questions

Las siguientes preguntas de ejemplo le ayudarán a familiarizarse con el formato de las preguntas del examen y con el contenido que pudiera cubrir el examen.


<style type="text/css">
    ol { list-style-type: upper-alpha; }
</style>

## Preguntas: 

1.Every employee of your company has a Google account. Your operational team needs to manage a large number of instances on Compute Engine. Each member of this team needs only administrative access to the servers. Your security team wants to ensure that the deployment of credentials is operationally efficient and must be able to determine who accessed a given instance. What should you do?



<ol type="a">
  <li>
    Generate a new SSH key pair. Give the private key to each member of your team. Configure the public key in the metadata of each instance.
  </li>
  <li>
    Ask each member of the team to generate a new SSH key pair and to send you their public key. Use a configuration management tool to deploy those keys on each instance.
  </li>
  <li>
    Ask each member of the team to generate a new SSH key pair and to add the public key to their Google account. Grant the ג€compute.osAdminLoginג€ role to the Google group corresponding to this team.
  </li> 
  <li>
    Generate a new SSH key pair. Give the private key to each member of your team. Configure the public key as a project-wide public SSH key in your Cloud Platform project and allow project-wide public SSH keys on each instance.
  </li> 
</ol>

2.You need to create a custom VPC with a single subnet. The subnet's range must be as large as possible. Which range should you use?

<ol type="a">
  <li>
  0.0.0.0/0
  </li>
  <li>
  10.0.0.0/8
  </li>
  <li>
    172.16.0.0/12
  </li> 
  <li>
    192.168.0.0/16
  </li> 
</ol>

3.You want to select and configure a cost-effective solution for relational data on Google Cloud Platform. You are working with a small set of operational data in one geographic location. You need to support point-in-time recovery. What should you do?

<ol type="a">
  <li>
  Select Cloud SQL (MySQL). Verify that the enable binary logging option is selected. Most Voted
  </li>
  <li>
  Select Cloud SQL (MySQL). Select the create failover replicas option.
  </li>
  <li>
    Select Cloud Spanner. Set up your instance with 2 nodes.
  </li> 
  <li>
    Select Cloud Spanner. Set up your instance as multi-regional.
  </li> 
</ol>

4.You want to configure autohealing for network load balancing for a group of Compute Engine instances that run in multiple zones, using the fewest possible steps.
You need to configure re-creation of VMs if they are unresponsive after 3 attempts of 10 seconds each. What should you do?


<ol type="a">
  <li>
Create an HTTP load balancer with a backend configuration that references an existing instance group. Set the health check to healthy (HTTP)
  </li>
  <li>
Create an HTTP load balancer with a backend configuration that references an existing instance group. Define a balancing mode and set the maximum RPS to 10.
  </li>
  <li>
Create a managed instance group. Set the Autohealing health check to healthy (HTTP)
  </li> 
  <li>
Create a managed instance group. Verify that the autoscaling setting is on.
  </li> 
</ol>

5.You are using multiple configurations for gcloud. You want to review the configured Kubernetes Engine cluster of an inactive configuration using the fewest possible steps. What should you do?

<ol type="a">
  <li>
Use gcloud config configurations describe to review the output.
  </li>
  <li>
Use gcloud config configurations activate and gcloud config list to review the output.
  </li>
  <li>
Use kubectl config get-contexts to review the output.
  </li> 
  <li>
Use kubectl config use-context and kubectl config view to review the output. 
  </li> 
</ol>

6.Your company uses Cloud Storage to store application backup files for disaster recovery purposes. You want to follow Google's recommended practices. Which storage option should you use?

<ol type="a">
  <li>
Multi-Regional Storage
  </li>
  <li>
Regional Storage
  </li>
  <li>
Nearline Storage
  </li> 
  <li>
Coldline Storage
  </li> 
</ol>

7.Several employees at your company have been creating projects with Cloud Platform and paying for it with their personal credit cards, which the company reimburses. The company wants to centralize all these projects under a single, new billing account. What should you do?

<ol type="a">
  <li>
Contact cloud-billing@google.com with your bank account details and request a corporate billing account for your company.
  </li>
  <li>
Create a ticket with Google Support and wait for their call to share your credit card details over the phone.
  </li>
  <li>
In the Google Platform Console, go to the Resource Manage and move all projects to the root Organizarion. Then, create a new billing account and set up a payment method.
  </li> 
  <li>
In the Google Cloud Platform Console, create a new billing account and set up a payment method.
  </li> 
</ol>

8.You have an application that looks for its licensing server on the IP 10.0.3.21. You need to deploy the licensing server on Compute Engine. You do not want to change the configuration of the application and want the application to be able to reach the licensing server. What should you do?

<ol type="a">
  <li>
Reserve the IP 10.0.3.21 as a static internal IP address using gcloud and assign it to the licensing server.
  </li>
  <li>
Reserve the IP 10.0.3.21 as a static public IP address using gcloud and assign it to the licensing server.
  </li>
  <li>
Use the IP 10.0.3.21 as a custom ephemeral IP address and assign it to the licensing server.
  </li> 
  <li>
Start the licensing server with an automatic ephemeral IP address, and then promote it to a static internal IP address.
  </li> 
</ol>

9.You are deploying an application to App Engine. You want the number of instances to scale based on request rate. You need at least 3 unoccupied instances at all times. Which scaling type should you use?

<ol type="a">
  <li>
Manual Scaling with 3 instances.  </li>
  <li>
Basic Scaling with min_instances set to 3.  </li>
  <li>
Basic Scaling with max_instances set to 3.  </li> 
  <li>
Automatic Scaling with min_idle_instances set to 3.  </li> 
</ol>

10.You have a development project with appropriate IAM roles defined. You are creating a production project and want to have the same IAM roles on the new project, using the fewest possible steps. What should you do?

<ol type="a">
  <li>
Use gcloud iam roles copy and specify the production project as the destination project.
  </li>
  <li>
Use gcloud iam roles copy and specify your organization as the destination organization.
</li>
  <li>
In the Google Cloud Platform Console, use the 'create role from role' functionality.
</li> 
  <li>
In the Google Cloud Platform Console, use the 'create role' functionality and select all applicable permissions.
</li> 
</ol>

11.You need a dynamic way of provisioning VMs on Compute Engine. The exact specifications will be in a dedicated configuration file. You want to follow Google's recommended practices. Which method should you use?

<ol type="a">
  <li>
Deployment Manager

  </li>
  <li>
Cloud Composer

</li>
  <li>
Managed Instance Group

</li> 
  <li>
Unmanaged Instance Group

</li> 
</ol>

12.You have a Dockerfile that you need to deploy on Kubernetes Engine. What should you do?

<ol type="a">
  <li>
Use kubectl app deploy <dockerfilename>.
  </li>
  <li>
Use gcloud app deploy <dockerfilename>.
</li>
  <li>
Create a docker image from the Dockerfile and upload it to Container Registry. Create a Deployment YAML file to point to that image. Use kubectl to create the deployment with that file. 
</li> 
  <li>
Create a docker image from the Dockerfile and upload it to Cloud Storage. Create a Deployment YAML file to point to that image. Use kubectl to create the deployment with that file.
</li> 
</ol>

13.Your development team needs a new Jenkins server for their project. You need to deploy the server using the fewest steps possible. What should you do?

<ol type="a">
  <li>
Download and deploy the Jenkins Java WAR to App Engine Standard.
  </li>
  <li>
Create a new Compute Engine instance and install Jenkins through the command line interface.
</li>
  <li>
Create a Kubernetes cluster on Compute Engine and create a deployment with the Jenkins Docker image.
</li> 
  <li>
Use GCP Marketplace to launch the Jenkins solution.
</li> 
</ol>

14.You need to update a deployment in Deployment Manager without any resource downtime in the deployment. Which command should you use?

<ol type="a">
  <li>
gcloud deployment-manager deployments create --config <deployment-config-path>
  </li>
  <li>
gcloud deployment-manager deployments update --config <deployment-config-path>
</li>
  <li>
gcloud deployment-manager resources create --config <deployment-config-path>
</li> 
  <li>
gcloud deployment-manager resources update --config <deployment-config-path>
</li> 
</ol>

15.You need to run an important query in BigQuery but expect it to return a lot of records. You want to find out how much it will cost to run the query. You are using on-demand pricing. What should you do?


<ol type="a">
  <li>
Arrange to switch to Flat-Rate pricing for this query, then move back to on-demand.
  </li>
  <li>
Use the command line to run a dry run query to estimate the number of bytes read. Then convert that bytes estimate to dollars using the Pricing Calculator.
</li>
  <li>
Use the command line to run a dry run query to estimate the number of bytes returned. Then convert that bytes estimate to dollars using the Pricing Calculator.
</li> 
  <li>
Run a select count (*) to get an idea of how many records your query will look through. Then convert that number of rows to dollars using the Pricing Calculator.
</li> 
</ol>

