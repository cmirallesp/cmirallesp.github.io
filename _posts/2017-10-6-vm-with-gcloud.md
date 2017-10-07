---
layout: post
title: Setup a remote machine with glcoud 
tags: gcloud google 
---

# Concepts

- **Projects:** each project has assigned a set of resources (repos, ...). You can run a console in the browser that run a virtual machine to manage such resources and execute commands.

- **Compute:** product to create virtual machines 

1. Create a project from gcloud console

2. Create a compute unit from console (select the instance type and the os image that suit better for you)

3. Connect to the new unit through ssh `gcloud compute --project "mai-tfm" ssh --zone "us-east4-a" "instance-tfm"`

4. Create a ssh key with `ssh-key` command

5. Add the key to the github repo

6. clone the repo  

Next steps is without compute unit, but instantiating a project from console (browser)
1. Create repository
	1. Enter in gcloud console [https://console.cloud.google.com](https://console.cloud.google.com])
	2. Go to source repositories/repositories create repository (REPO_NAME)
	3. Select mirror and select github and fill out the repo url 


2. Clone repo in your project
`gcloud source repos clone \<REPO_NAME\> --project= \<project-id\>`




