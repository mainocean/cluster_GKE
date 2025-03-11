# Raising a Cluster in GKE

[<img src="assets/GKE.png?raw=true">](https://www.youtube.com/watch?v=I4UKAeKV4WQ)

Hi. In this video I setting up a Cluster in GKE. To raise a cluster in Google Kubernetes Engine, i follow these general steps: installing SDK, kubect. Raising a cluster in Google Kubernetes Engine (GKE) involves creating and configuring a Kubernetes cluster on Google's cloud infrastructure. It's a process that allows you to deploy, manage, and scale containerized applications efficiently. The steps typically include enabling the Kubernetes API, choosing your cluster type (zonal or regional), setting the desired configurations, and creating the cluster through the Google Cloud Console or command-line tools like gcloud. Once your cluster is set up, you can connect to it and deploy your workloads using Kubernetes manifests.

https://www.youtube.com/watch?v=I4UKAeKV4WQ

# Need for install:

```
Google Cloud SDK    https://shorturl.at/oXVka
kubectl             https://shorturl.at/WR2Q9
                    https://kubernetes.io/releases/download/#binaries
```

# Console commands:

```
echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list

sudo apt-get -y install apt-transport-https ca-certificates gnupg
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -

sudo apt update
sudo apt-get install -y google-cloud-sdk
gcloud init
sudo apt install kubectl
kubectl version --client
gcloud services enable container.googleapis.com
gcloud container clusters create alex1 --zone europe-west3-a
gcloud container clusters get-credentials alex1 --zone europe-west3-a

gcloud container node-pools create np1 --cluster alex1 --zone europe-west3-a --machine-type e2-medium

gcloud container clusters create alex1 --zone europe-west3-a --machine-type e2-micro

gcloud container clusters create alex1 --zone europe-west3-a --machine-type e2-micro

gcloud container clusters delete my-first-cluster-1 --zone europe-west3-a
```

# Social

🎥 - [YouTube](https://www.youtube.com/c/AntonPutra)  
💼 - [LinkedIn](https://www.linkedin.com/in/anton-putra)  
🛠️ - [Twitter/X](https://x.com/antonvputra)  
🙋‍♂️ - [Instagram](https://www.instagram.com/aputrabay)  
📨 - me@antonputra.com
