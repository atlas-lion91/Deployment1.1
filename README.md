<p align="center">
<img src="https://github.com/kura-labs-org/kuralabs_deployment_1/blob/main/Kuralogo.png">
</p>
<h1 align="center">C4_deployment-1.1<h1> 

## Instructions:

Demonstrate your ability to run a Jenkins build and manually deploy to Elastic Beanstalk.
Once you deploy, your deployment to elastic beanstalk will fail or you will see a degraded health status.
Find and correct the issue to execute deployment.



## Documentation:

### Download Application Files:

1. Download the zipped application files from the instructor's GitHub repository.
2. Extract the downloaded zip file to your local directory.

### Setup New GitHub Repository:

1. Create a new GitHub repository to host the application.
2. Upload the application files to the new repository.
3. Do not upload the parent folder, instead compress all application files within parent folder.

### Setup Jenkins Pipeline:

1. Log in to the instructor-provided Jenkins Server.
2. Create a new Jenkins build pipeline for the application.
3. Configure the pipeline to fetch the code from the newly created GitHub repository.
4. Run the Jenkins pipeline Build.
5. Test the Jenkins build to ensure successful execution.

### Create the Application Source Bundle:

- Select the application files in your local directory and compress them into a Zip folder.
- This creates a source bundle that will be used for deployment on AWS Elastic Beanstalk.

### Create IAM Roles & Permissions:

1. Log in to your AWS Management Console.
2. Create new IAM Roles for your environment
3. Setup permissions to allow the application to interact with AWS services.
4. Assign these permissions to the applicable IAM roles.

### Setup and Execute Manual Application Deployment on Elastic Beanstalk:

1. Log in to your AWS Management Console.
2. Navigate to AWS Elastic Beanstalk.
3. Configure the Elastic Beanstalk environment for your application.
4. Upload and deploy the application source to the Elastic Beanstalk environment.
5. Monitor the process and ensure the application properly executes.
 

![Screenshot 2023-08-16 221846](https://github.com/atlas-lion91/Deployment1.1/assets/140761974/56b2e06e-1981-471d-b0a1-3ddf9347077d)




## *Errors & Corrections*: 
- After intial deployment of the application, the environment health shows "degraded".
  

![Screenshot 2023-08-16 214125](https://github.com/atlas-lion91/Deployment1.1/assets/140761974/40e7c04d-07d1-47a6-9566-28dd04d8e730)


  
- Observed the ElasticBeanstalk logs, and located the error [ModuleNotFoundError: No module named 'application']  in the /var/log/web.stdout.log section.


![Deployment 1 1 Elastic Beanstalk Logs](https://github.com/atlas-lion91/Deployment1.1/assets/140761974/8fb2f654-b1aa-42ea-b737-1e3c2357f182)


- Re-Named the app.py file "application.py".
- Re-Uploaded the application to Elastic Beanstalk with the renamed application.py file.
- The Environment health status read "OK" and the application deployed successfully.


![Deployment 1 1 confirmation](https://github.com/atlas-lion91/Deployment1.1/assets/140761974/2b2066a4-96d6-4319-9280-5f969c4938c6)
