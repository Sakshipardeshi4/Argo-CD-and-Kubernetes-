
Overview
Engineered a declarative CI/CD pipeline using **Argo CD** and **GitOps** principles to manage containerized applications on AWS. This project ensures high availability and system reliability through automated synchronization.

Technical Stack
* **Cloud:** AWS (EKS, VPC, IAM)
* **Orchestration:** Kubernetes 
* **GitOps:** Argo CD 
* **Observability:** Prometheus & Grafana

Key Achievements
* **99.9% Availability:** Guaranteed through active health checks and Kubernetes workload orchestration.
* **Real-time Monitoring:** Designed custom Grafana dashboards to visualize cluster health, CPU, and Memory usage.
  <p align="center">
  <img src="images/grafana dashboard.png" width="600">
</p
  * **Real-time Argo CD pipeline visualization:**
  <p align="center">
  <img src="images/argo cd pipeline.png" width="600">
</p
* **Kubernetes Dashboard**
  <p align="center">
  <img src="images/k8s dashboard.png" width="600">
</p>
* **Prometheus Metrics Graph**
   <p align="center">
  <img src="images/prometheus metrics.png" width="600">
</p>



Challenges & Troubleshooting
* **Issue:** **ImagePullBackOff** errors in the EKS cluster.
  * **Cause:** The worker nodes lacked IAM permissions to pull images from the private ECR.
  * **Solution:** Updated the IAM Role policy to include AmazonEC2ContainerRegistryReadOnly.
* **Issue:** **OOMKilled** pods in Prometheus.
  * **Solution:** Implemented Resource Limits/Requests and adjusted data retention periods to optimize memory.
  

