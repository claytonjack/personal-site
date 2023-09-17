---
title: "Optimizing My Workflow With Infrastructure as Code"
date: 2023-09-05T06:00:23+06:00
hero: images/hero/infrastructure-as-code.jpg
description: "My experience using Infrastructure as Code tools"
theme: Toha
menu:
    sidebar:
        name: "Infrastructure as Code"
        identifier: infrastructure-as-code
        weight: 500
---

### Docker Compose

Following my transition from Unraid, I needed a better way to manage my Docker containers. Very quickly, I discovered docker-compose and instantly adopted it as my preferred method for container management. Docker-compose utilizes declarative YAML files to define the configuration of your containers. This method of management, and ones like it, is what's known as Infrastructure as Code (IaC), a concept that has become increasingly popular in recent years. This solution has revolutionized my approach to system management as it allows me to store my configuration files in a Git repository, ensuring a streamlined process for deploying my configured services on a new machine in the case of failure.

{{< img src="/posts/images/infrastructure-as-code/docker-compose.jpg" height="400" width="600" align="center" title="Docker Compose" >}}

### Packer

After having such a great experience with Docker Compose, I wanted to learn additional tools that could make my life easier. I decided to start with the HashiCorp suite of products, with Packer being my starting point. I integrated Packer seamlessly with Proxmox thanks to the following [builder](https://developer.hashicorp.com/packer/integrations/hashicorp/proxmox) from Hashicorp, allowing me to effortlessly create customized, pre-built virtual machine images. Once I am finished defining the image, a single command is all that is needed to install, and convert the image to a template, making future deployments a breeze.

{{< img src="/posts/images/infrastructure-as-code/packer.jpg" height="400" width="600" align="center" title="Packer" >}}

### Terraform

Now that I had my template ready to go, I needed a way to automate the provisioning of system resources for deployment. The solution to this was Terraform. Terraform works similarly to Packer in that it utilizes declarative configuration files to define the desired state of your infrastructure. For this to work with Proxmox, I needed to use the following [provider](https://registry.terraform.io/providers/Telmate/proxmox/latest). Once I had the provider installed, Terraform made it easy to define anything from system memory, CPU cores, and networking, without having to use the Web-UI.

{{< img src="/posts/images/infrastructure-as-code/terraform.jpg" height="400" width="600" align="center" title="Terraform" >}}

### Cloud-init

The real magic of my Hashicorp workflow is down to the use of Cloud-init. Cloud-init allows for dynamic configuration of VMs, including user info, IP addresses, and SSH keys. This becomes a necessity in a business environment as often you will be dealing with people who each have specific requirements for the VM. When defining my image with Packer, I tell it to provision the template with Cloud-Init Integration. Then, once I am ready to clone the template, I can use Terraform to pass on the necessary variables to create a customized VM for each install.

{{< img src="/posts/images/infrastructure-as-code/cloud-init.jpg" height="400" width="600" align="center" title="Cloud-init" >}}
