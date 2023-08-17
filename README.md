<p align="center">
<img src="https://github.com/kura-labs-org/kuralabs_deployment_1/blob/main/Kuralogo.png">
</p>
<h1 align="center">C4_deployment-1.1<h1> 

## Instructions:

Demonstrate your ability to run a Jenkins build and manually deploy to Elastic Beanstalk.
Once you deploy, your deployment to elastic beanstalk will fail or you will see a degraded health status.
Find and correct the issue to execute deployment.

## Documentation:

### 1: Download Zip Folder and Extract Application Files

1. Download the zipped application files from the instructor's GitHub repository.
2. Extract the downloaded zip file to your local directory.

### 2: Setup New GitHub Repository

1. Create a new GitHub repository to host the application.
2. Upload the application files to the new repository.
3. Do not upload the parent folder, instead compress all application files within parent folder.

### 3: Setup Jenkins Pipeline

1. Log in to the instructor-provided Jenkins Server.
2. Create a new Jenkins build pipeline for the application.
3. Configure the pipeline to fetch the code from the newly created GitHub repository.
4. Run and test the Jenkins build pipeline to ensure successful execution.

### 4: Create Application Source Bundle

- Compress the application files to create a source bundle.
- This source bundle will be used for deployment on AWS Elastic Beanstalk.

### 5: Create IAM Roles & Permissions

1. Log in to your AWS Management Console.
2. Create new IAM Roles and setup permissions to allow the application to interact with AWS services.
3. Assign these permissions to the applicable IAM roles.

### 6: Setup and Execute Application Deployment on Elastic Beanstalk

1. Log in to your AWS Management Console.
2. Navigate to AWS Elastic Beanstalk.
3. Configure the Elastic Beanstalk environment for your application.
4. Upload and deploy the application source to the Elastic Beanstalk environment.
5. Monitor the process and ensure the application properly executes.
 


## Errors & Correction: 
- After intial deployment of the application, the environment health shows "degraded". 
- Observed the ElasticBeanstalk logs, and located the error [ModuleNotFoundError: No module named 'application']  in the /var/log/web.stdout.log section.
- Re-Named the app.py file "application.py".
- Re-Uploaded the application to Elastic Beanstalk with the renamed application.py file.
- The Environment health status read "OK" and the application deployed successfully.
