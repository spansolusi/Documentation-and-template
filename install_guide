**Minimum system requirements for minikube**

- 2 GB RAM or more
- 2 CPU / vCPU or more
- 20 GB free hard disk space or more
- Docker / Virtual Machine Manager – KVM &amp; VirtualBox

**Step 1) Apply updates**

Apply all updates of existing packages of your system by executing the following apt commands

$ sudo apt-get update &amp;&amp; sudo apt upgrade -y

![](RackMultipart20220407-4-1yxd61o_html_92f678e438e94bca.png)

**Step 2) Install Minikube dependencies**

Install the following minikube dependencies by running beneath command,

$ sudo apt install -y curl wget apt-transport-https

![](RackMultipart20220407-4-1yxd61o_html_f5c8d7ba55cf1981.png)

**Step 3) Download Minikube Binary**

Use the following wget command to download latest minikube binary,

$ wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

![](RackMultipart20220407-4-1yxd61o_html_c2362dcd32d388ea.png)

Once the binary is downloaded, copy it to the path /usr/local/bin and set the executable permissions on it

$ sudo cp minikube-linux-amd64 /usr/local/bin/minikube

$ sudo chmod +x /usr/local/bin/minikube

![](RackMultipart20220407-4-1yxd61o_html_ccc57138ae2295cf.png)

Verify the minikube version

$ minikube version

![](RackMultipart20220407-4-1yxd61o_html_978a8247b924adac.png)

**Step 4) Install Kubectl utility**

Kubectl is a command utility which is used to interact with Kubernetes cluster for managing deployments, service and pods etc. Use below curl command to download latest version of kubectl.

$ curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl

![](RackMultipart20220407-4-1yxd61o_html_4d490bc883292f57.png)

Once kubectl is downloaded then set the executable permissions on kubectl binary and move it to the path /usr/local/bin.

$ chmod +x kubectl

$ sudo mv kubectl /usr/local/bin/

![](RackMultipart20220407-4-1yxd61o_html_ee8484532c67f1c5.png)

Now verify the kubectl version

$ kubectl version -o yaml

![](RackMultipart20220407-4-1yxd61o_html_b3be3d8f5ae8ed7e.png)

**Step 5) Start the minikube**

As we are already stated in the beginning that we would be using docker as base for minikue, so start the minikube with the docker driver,

$ minikube start

Or if you want start minikube on docker image, run this command

$ minikube start --driver=docker

![](RackMultipart20220407-4-1yxd61o_html_81f48aa87fc91bfd.png)

# **CLI:**

**Update &amp; upgrade**

sudo apt-get update &amp;&amp; sudo apt upgrade -y

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
