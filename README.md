## Deploying “Stan’s Robot Shop” eCommerce Application on AWS EKS

The Stan’s Robot Shop application is a 3-Tier architecture consisting of a web front end, application logic, and a database tier. It is deployed on Amazon Elastic Kubernetes Service (EKS), taking advantage of the scalability, flexibility, and managed Kubernetes environment provided by AWS. This setup ensures efficient resource management, high availability, and auto-scaling capabilities.

Components of the Architecture:

	1.Frontend :
	          The UI is developed as a containerized microservice, which interacts with customers. It is exposed using a Kubernetes Ingress with AWS ALB (Application Load Balancer)  to route incoming traffic.
	2.Backend :
	        Application logic is separated into microservices, each deployed as containers within EKS. Kubernetes manages the services, ensuring load balancing and seamless scaling.
	3.Database :
	        The backend database for managing product listings, customer data, and orders.

 Deployment Features:

	•	Cluster Management with eksctl: The entire EKS cluster is provisioned and managed using eksctl, an easy-to-use CLI tool that simplifies Kubernetes cluster creation and resource management.
 
	•  	Helm: Helm is used to manage and deploy the entire application, including the frontend, backend, and any supporting services. By packaging each component as a Helm chart, you can define Kubernetes resources declaratively, enabling easy updates, rollbacks, and scalability. Helm charts simplify the deployment process by automating the creation of Kubernetes resources such as deployments, services, config maps, and Ingress resources.
 
 	•	Security & Compliance: IAM roles and policies are integrated into the deployment using eksctl, ensuring secure access to AWS resources while maintaining compliance.
  
  	•	AWS ALB Controller: The AWS ALB Controller is integrated with Kubernetes Ingress to automatically provision an Application Load Balancer (ALB) when Ingress resources are created. 
   
	•	Kubernetes Ingress: Kubernetes Ingress allows you to expose the services within the cluster to the internet.
	
This architecture provides a robust, scalable, and secure environment for running the Stan’s Robot Shop application, ensuring a smooth customer experience.

## Sample Screenshots

<img width="1440" alt="1" src="https://github.com/user-attachments/assets/d9beee9f-ee14-4d37-aa9d-74701d2d830b">
<img width="1440" alt="2" src="https://github.com/user-attachments/assets/8ad948c3-c0e4-450c-990a-d3ad64e5e241">
<img width="1440" alt="3" src="https://github.com/user-attachments/assets/6a9bce7d-7422-4a78-b030-5cebb29d0f15">
<img width="1440" alt="4" src="https://github.com/user-attachments/assets/387384b5-cca9-4b45-8a55-f0663c2d9ce8">
<img width="1440" alt="5" src="https://github.com/user-attachments/assets/f1b3fbe3-8413-4b46-9197-247c483e3a1e">
<img width="1440" alt="6" src="https://github.com/user-attachments/assets/f7f792b0-fcd6-4604-9190-92788e118881">
<img width="1440" alt="7" src="https://github.com/user-attachments/assets/8a8e41d5-6c0d-4782-ae7d-02eb06c88828">
<img width="1440" alt="8" src="https://github.com/user-attachments/assets/bdd178ec-086d-4593-9bb8-39afbc64c789">
<img width="1440" alt="9" src="https://github.com/user-attachments/assets/6dbd259d-f9ec-4cad-b44e-ec983e095ae3">
<img width="1440" alt="10" src="https://github.com/user-attachments/assets/88807990-1656-49cd-baac-29bde7984de1">
<img width="1440" alt="11" src="https://github.com/user-attachments/assets/e61954bd-5187-4e3d-86a8-a5752fd0151a">
<img width="1440" alt="12" src="https://github.com/user-attachments/assets/96b1133c-7171-469f-9347-f0876f8a3790">











