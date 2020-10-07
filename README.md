# Introduction

## **Getting Started with Docker 101**

Welcome to the a Docker 101 learning challenge. In this challenge you will learn the fundamentals of Docker by completing this Docker 101 hands-on learning challenge. Once you are done with the learning labs, [answer the quiz questions](https://ibmcoders.ibmviprewards.ibm.com/channels/239) \(Hands-on Docker 101\) to test you knowledge.

### **Pre-requisites**

To complete the workshop labs included in this challenge, you will need to:

* Create or have an [IBM Cloud account](https://volaka.gitbook.io/ibm-cloud-registration/).
* Have basic knowledge of [Linux](https://developer.ibm.com/tutorials/linux-basics-and-commands/). 

Read the tutorial ["Containerization: Starting with Docker and IBM Cloud"](https://developer.ibm.com/tutorials/building-docker-images-locally-and-in-cloud/) or follow this guide. 

This tutorial provides an introduction to Docker commands, Dockerfiles, and using Docker with the IBM Cloud Container Registry.

### **Steps**

In the labs you will get hands on experience with:

> * Setting up Docker
> * Running your first container and clean up once you are done
> * Creating and publishing custom images
> * Orchestration with Docker Swarm

Clone the GitHub repository and follow labs 0-3 included in the tutorial: [https://github.com/IBM/intro-to-docker-lab](https://github.com/IBM/intro-to-docker-lab). This tutorial is the customize tutorial of official IBM Docker Lab 101

![](https://avatars0.githubusercontent.com/u/1459110?s=400&v=4)

## Outline

* lab0 - [Install Docker](https://github.com/volaka/intro-to-docker-lab/tree/6812e5acd913afcf01957885b524dd13ec13ff50/lab0.md)
* lab1 - [Run your first container](https://github.com/volaka/intro-to-docker-lab/tree/6812e5acd913afcf01957885b524dd13ec13ff50/lab1.md)
* lab2 - [Add value with custom images](https://github.com/volaka/intro-to-docker-lab/tree/6812e5acd913afcf01957885b524dd13ec13ff50/lab2.md)
* lab3 - [introduction to orchestration](https://github.com/volaka/intro-to-docker-lab/tree/6812e5acd913afcf01957885b524dd13ec13ff50/lab3.md)
=======
# Docker
Series of labs and instructions to introduce you to containers and Docker. Learn to run a container, inspect a container and understand the isolation of processes, create a Dockerfile, build an image from a Dockerfile and understand layers, tag and push images to a registry, scale and update containers, and more.

To view the Docker workshop online, go to:
* <https://ibm-developer.gitbook.io/docker101/>.

To view the Docker workshop in Github, go to:
* [workshop/README.md](workshop/README.md).

This repository has the following structure:
```ini
- workshop (workshop labs)
|_ .gitbook (images)
|_ <language> (localization support) 
  |_ <folder-n> (workshop labs)
    |_README.md (steps for labs in Markdown)
  |_ README.md (gitbook home page)
  |_ SUMMARY.md (table of contents)
.gitbook.yaml (GitBook read-only instructions)
.travis.yaml (runs markdownlint by default)
README.md (GitHub.com README)
```

## Markdown lint tool

Install the [Markdown lint tool](https://github.com/markdownlint/markdownlint),
```
$ npm install -g markdownlint-cli
```

To use markdownlint, run the following command,
```
$ markdownlint workshop -c ".markdownlint.json" -o mdl-results.md
```

## Build Gitbook 

Install the [gitbook-cli](https://github.com/GitbookIO/gitbook-cli),
```
$ npm install -g gitbook-cli
```

To build the Gitbook files into the `_book` sub-directory with the `gitbook-cli`, run the following command,
```
$ gitbook build ./workshop
```

Serve the Gitbook files locally with the following command,
```
$ gitbook serve ./workshop
```
