# An ASP .Net Core based Web Application used for testing the Microsoft Aure Pipelines setup.
<br>


### Related articles:
 - [develop an ASP .Net Core web application and containerize it with Docker](https://www.quickdevnotes.com/deploy-net-core-web-application-using-azure-and-docker/)
 - [setup Continuous Integration with Microsoft Azure DevOps Pipeline and GitHub](https://www.quickdevnotes.com/setup-microsoft-azure-build-pipeline/)
 - [setup Continuous Deployment pipeline to deploy the application as Docker container on Azure Web App Service](https://www.quickdevnotes.com/setup-release-pipeline-with-azure-devops/)


Commands
-------------

NOTE: This is an ASP.NET Core Version 2, it doesn't work on Version 5 SDK.

docker build -t webapp .
docker run -d -p 5000:80 --rm -it --name webapp webapp

docker tag webapp quickdevnotes/webapp:v1
docker login
docker push quickdevnotes/webapp:v1