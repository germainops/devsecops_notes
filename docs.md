## # DevSecOps Project 1

➡️ **SAST**: STATIC APPLICATION SECURITY TESTING 
➡️ **DAST**: DYNAMIC APPLICATION SECURITY TESTING
➡️ **SDLC**: SOFTWARE DEVELOPMENT LIFE CYCLE
➡️ **VM**: VIRTUAL MACHINE
➡️ **CI**: CONTINUOUS INTEGRATION
➡️ **CD**: CONTINOUS DEPLOYMENT

This my first devsecops project. These are the steps of the project 

1- Get the project repo 
2- Setup Github Actions 
3- Add VM Runner
4- Write a CI/CD Pipeline (Security Checks,Tests Cases, Build the app, Publish the artifact, Scan Docker Image, Push to Git, Deploay to K8)
5- Usins SAST, DAST Tools 

---

**NOTE 1**: The CI/CD Pipeline depends of the project stack. Here we have Java Project so i will write with maven.

**NOTE 2**: Each job that i need to run, needs a different environment.

I got the repo (like clone the app) and i pushed it in my own repo. After that i started writing my CI/CD Pipeline little by little, got my first error ans resolve it. 

Now i want to move foward by adding security check... For that i need to use **[Trivy](https://trivy.dev/docs/latest/getting-started/installation/)**  and **[Gitleaks](https://github.com/gitleaks/gitleaks)** for it. This documentation show how i add command for **[Trivy](https://trivy.dev/docs/latest/getting-started/installation/)** installation.

**[Gitleaks](https://github.com/gitleaks/gitleaks)** will help me detect and found if possible secrets like passwords, API keys, and tokens in git repos, files, and whatever else you wanna throw at it via stdin.


So i setup a private runner with AWS to have a separate runner instead of using the github runner. 


After that i updated the pipeline to be able to do the security checks with **Trivy** and **Gitleaks**. After a some failed ❌ i got a sucess ✅



Now i want to update the pipelie to run test unit cases and run [**SonarQube**](https://github.com/SonarSource/sonarqube).

[**SonarQube**](https://github.com/SonarSource/sonarqube) provides the capability to not only show the health of an application but also to highlight issues newly introduced

After several failed test, wheter with SonnarQube or AWS Instance. Everything went good and i got the image. So now i want tos etup EKS Cluster using Terraform.















