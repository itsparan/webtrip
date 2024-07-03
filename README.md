A CI/CD pipeline consists of the following steps:

Source control: The code is stored in a source control repository, such as GitHub or GitLab.
Build: The code is built into a deployable artifact, such as a Docker image or a JAR file.
Test: The artifact is tested to ensure that it works as expected.

Tech Used
GitHub: used web platform for version control and collaboration.
AWS CodeCommit: A managed source control service that provides secure and scalable hosting for private Git repositories.
AWS CodeBuild: A fully managed CI/CD service that compiles, tests, and packages code, automating the build process and ensuring code quality.
AWS CodePipeline: An automated CI/CD service that orchestrates and visualizes the software delivery process, seamlessly integrating various stages.


Step 4. Using AWS CodePipeline with GitHub
Go to the AWS console and search for CodePipeline.
Click on Create Pipeline and give your pipeline a name. Then, click Next.

Pipeline Creation
3. To connect CodePipeline to GitHub, follow these steps:

Open the Developer Tools console at https://console.aws.amazon.com/codesuite/settings/connections.
Under “Select a provider,” choose “GitHub.”
Click “Connect to GitHub” and follow the instructions.
4. Once GitHub is connected, go back to CodePipeline and do the following:

Under “Source provider,” choose “GitHub"
select the GitHub connection that you just created.
Select the name of the repository that holds your project’s source code.
Select the branch name that you want to use for the pipeline.
Click Next.

Prompt create a connection
5. For building, choose AWS CodeBuild and click Create Project. Follow the instructions given on the page to create a CodeBuild project.

6. In the Deploy section, select the deployment target. This could be an Amazon EC2 instance, an Amazon ECS service, or an Amazon S3 bucket.

Click Create to create the CI/CD pipeline.

Once the CI/CD pipeline is created, it will automatically trigger a build whenever there are changes to the source code in your GitHub repository. 


