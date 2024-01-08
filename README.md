# kubernetes-miniport
Deploying a Simple Application on Kubernetes

# Miniport Website on Kubernetes

[![GitHub Stars](https://img.shields.io/github/stars/Corletey/kubernetes-miniport?style=social)](https://github.com/Corletey/kubernetes-miniport)
[![GitHub Forks](https://img.shields.io/github/forks/Corletey/kubernetes-miniport?style=social)](https://github.com/Corletey/kubernetes-miniport/fork)

**Description:**

This repository contains the Kubernetes YAML files for deploying the Miniport website using Kubernetes. The Miniport website is a static website hosted within a Docker container.

**Getting Started:**

1. **Prerequisites:**
   - [Minikube](https://minikube.sigs.k8s.io/docs/start/) installed on your local machine.
   - [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) installed on your local machine.

2. **Deployment:**
   - Clone the repository:
     git clone https://github.com/Corletey/kubernetes-miniport.git
     cd kubernetes-miniport

   - Apply the deployment and service YAML files:
     kubectl apply -f deployment.yaml
     kubectl apply -f service.yaml

3. **Access the Miniport Website:**
   - Get the external IP of the service:
     kubectl get services miniport-service

   - Access the Miniport website using the external IP and the defined port.

**Container Lifecycle Management:**

The deployment.yaml file includes configurations for:

- Rolling Updates: Ensures updates with minimal downtime.
- Probes: Implements readiness and liveness probes.
- Pod Disruption Budget: Limits disruptions during voluntary disruptions.

**Contributing:**

If you'd like to contribute to this project, please follow the standard GitHub workflow:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/new-feature`).
3. Make changes and commit (`git commit -m "Add new feature"`).
4. Push the branch (`git push origin feature/new-feature`).
5. Create a pull request.

**Authors:**

- Corletey(https://github.com/Corletey) - Project Contributor

**License:**

This project is licensed under the [MIT License](LICENSE).

**Additional Information:**

- For more details on the Miniport website, refer to the [original repository](https://github.com/Corletey/static-website-docker).
