# Deploy to EKS Cluster from Jenkins
This guide outlines the steps to set up Jenkins for deploying applications to an Amazon EKS (Elastic Kubernetes Service) cluster. The deployment process involves installing necessary tools on the Jenkins container, configuring AWS authentication, and adjusting the Jenkinsfile for EKS cluster deployment.

## Create a cluster using eksctl 
Utilize eksctl to establish the requisite environment for running the Kubernetes cluster. Employing eksctl in this project ensures a streamlined and efficient setup of the Kubernetes cluster, simplifying the deployment process.The installation guide is available in the AWS documentation and can be accessed using the following URL.https://eksctl.io/installation/

![eks2](https://github.com/busolagbadero/Deploy-to-EKS-cluster-from-Jenkins/assets/94229949/86d05be7-fb16-4343-ac9f-7b69f49465c1)

![eks3](https://github.com/busolagbadero/Deploy-to-EKS-cluster-from-Jenkins/assets/94229949/dda87a2c-03e7-4ba7-830e-b701f448190b)

![eks4](https://github.com/busolagbadero/Deploy-to-EKS-cluster-from-Jenkins/assets/94229949/f2ec72a6-fe2b-49a7-91aa-f094cfe1f6be)


## Create a jenkins Server. 
In this project, the incorporation of a Jenkins server plays a crucial role in optimizing the continuous integration and continuous deployment (CI/CD) workflow. Docker is employed to initiate a container, within which the necessary tools are installed.

![eks7](https://github.com/busolagbadero/Deploy-to-EKS-cluster-from-Jenkins/assets/94229949/c932c318-354c-401d-ad09-7168fa802880)


## Install Kubectl on Jenkins Server.
The installation of kubectl on the Jenkins server is crucial as it serves as the command-line tool for interacting with Kubernetes clusters, including Amazon EKS (Elastic Kubernetes Service). This is an essential step in the deployment process, where kubectl commands are employed to effectively manage and deploy applications to Kubernetes clusters.

The installation guide is available in the AWS documentation and can be accessed using the following URL.https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html

![eks5](https://github.com/busolagbadero/Deploy-to-EKS-cluster-from-Jenkins/assets/94229949/5953db81-63eb-4d42-baa3-47b60512fa74)

## Install iam-authenticator on Jenkins Container
Installing iam-authenticator on the Jenkins container is imperative for this project to enable secure authentication with AWS services. iam-authenticator facilitates seamless communication between Jenkins and Amazon EKS, ensuring secure access to the Kubernetes cluster. This authentication mechanism is integral to the overall project workflow, enhancing the security posture and enabling proper interaction with AWS resources during the deployment process.
The installation can be accessed using the following URL. https://weaveworks-gitops.awsworkshop.io/60_workshop_6_ml/00_prerequisites.md/50_install_aws_iam_auth.html

![eks6](https://github.com/busolagbadero/Deploy-to-EKS-cluster-from-Jenkins/assets/94229949/3d6638ad-421e-4742-8b23-573accd3a0e1)

## Create kubeconfig File
