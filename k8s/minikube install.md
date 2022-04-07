**Minimum system requirements for minikube**

- 2 GB RAM or more
- 2 CPU / vCPU or more
- 20 GB free hard disk space or more
- Docker / Virtual Machine Manager – KVM & VirtualBox

**Step 1) Apply updates**

Apply all updates of existing packages of your system by executing the following apt commands

$ sudo apt-get update && sudo apt upgrade -y

![](Aspose.Words.179b1b75-91f8-4f92-9a90-6059d5a70639.001.png)

**Step 2) Install Minikube dependencies**

Install the following minikube dependencies by running beneath command,

$ sudo apt install -y curl wget apt-transport-https

![](Aspose.Words.179b1b75-91f8-4f92-9a90-6059d5a70639.002.png)


**Step 3) Download Minikube Binary**

Use the following wget command to download latest minikube binary,

$ wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

![](Aspose.Words.179b1b75-91f8-4f92-9a90-6059d5a70639.003.png)

Once the binary is downloaded, copy it to the path /usr/local/bin and set the executable permissions on it

$ sudo cp minikube-linux-amd64 /usr/local/bin/minikube

$ sudo chmod +x /usr/local/bin/minikube

![](Aspose.Words.179b1b75-91f8-4f92-9a90-6059d5a70639.004.png)

Verify the minikube version

$ minikube version

![](Aspose.Words.179b1b75-91f8-4f92-9a90-6059d5a70639.005.png)

**Step 4) Install Kubectl utility**

Kubectl is a command utility which is used to interact with Kubernetes cluster for managing deployments, service and pods etc. Use below curl command to download latest version of kubectl.

$ curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl

![](Aspose.Words.179b1b75-91f8-4f92-9a90-6059d5a70639.006.png)


Once kubectl is downloaded then set the executable permissions on kubectl binary and move it to the path /usr/local/bin.

$ chmod +x kubectl

$ sudo mv kubectl /usr/local/bin/

![](Aspose.Words.179b1b75-91f8-4f92-9a90-6059d5a70639.007.png)

Now verify the kubectl version

$ kubectl version -o yaml

![](Aspose.Words.179b1b75-91f8-4f92-9a90-6059d5a70639.008.png)

**Step 5) Start the minikube**

As we are already stated in the beginning that we would be using docker as base for minikue, so start the minikube with the docker driver,

$ minikube start 

Or if you want start minikube on docker image, run this command

$ minikube start --driver=docker

![](Aspose.Words.179b1b75-91f8-4f92-9a90-6059d5a70639.009.png)

**CLI:**

**Update & upgrade**

sudo apt-get update && sudo apt upgrade -y

**Install Dependencies**

sudo apt install -y curl wget apt-transport-https

**Download Minikube Binary**

wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

sudo cp minikube-linux-amd64 /usr/local/bin/minikube

sudo chmod +x /usr/local/bin/minikube

**Install Kubectl** 

curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl

chmod +x kubectl

sudo mv kubectl /usr/local/bin/

**Start the minikube**

minikube start --driver=docker

