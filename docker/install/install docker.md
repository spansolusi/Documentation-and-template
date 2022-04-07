Step 1 — Installing Docker

First, update your current package list:

$ sudo apt update

![](Aspose.Words.05f9d7cf-161f-4d3f-a2dd-15557bb54c05.001.png)

Next, install some prerequisite packages that allow apt to use packages over HTTPS:

$ sudo apt install apt-transport-https ca-certificates curl software-properties-common

![](Aspose.Words.05f9d7cf-161f-4d3f-a2dd-15557bb54c05.002.png)

Then add the GPG key for the official Docker repository to your system:

$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add –

![](Aspose.Words.05f9d7cf-161f-4d3f-a2dd-15557bb54c05.003.png)

Add the Docker repository to the APT source:

$sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"

![](Aspose.Words.05f9d7cf-161f-4d3f-a2dd-15557bb54c05.004.png)

Next, update the packages database with the Docker packages from the newly added repo:

$sudo apt update

![](Aspose.Words.05f9d7cf-161f-4d3f-a2dd-15557bb54c05.005.png)

Make sure you are going to install from the Docker repo instead of the default Ubuntu repo:

$apt-cache policy docker-ce

You should see output like this, although the version numbers for Docker may be different: ![](Aspose.Words.05f9d7cf-161f-4d3f-a2dd-15557bb54c05.006.png)

Note that docker-ce is not installed yet, but a candidate for installation is from the Docker repository for Ubuntu 20.04 (focal).

Finally, install Docker:

$sudo apt install docker-ce

![](Aspose.Words.05f9d7cf-161f-4d3f-a2dd-15557bb54c05.007.png)

.

.

.

Docker should now be installed, the daemon started, and the process should now be able to run on startup at boot. Check that it's running:

$sudo systemctl status docker

The output should be similar to the following, indicating that the service is up and running:

![](Aspose.Words.05f9d7cf-161f-4d3f-a2dd-15557bb54c05.008.png)
