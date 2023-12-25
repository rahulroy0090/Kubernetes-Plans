
[What are the basic components of Docker?](#what-are-the-basic-components-of-docker)
[Difference between containerization and virtual machines.](#difference-between-containerization-and-virtual-machines)

[Why do we use containerization?](#why-do-we-use-containerization)

[Difference between a container and a pod.
](#difference-between-a-container-and-a-pod)
 
[How Docker storage and networking work.](#how-docker-storage-and-networking-work)

[What is runtime in containerization and what are the types in containerization?](#what-is-runtime-in-containerization-and-what-are-the-types-in-containerization)

[#Difference between low-level and high-level runtime in containerization.](#difference-between-low-level-and-high-level-runtime-in-containerization)

[Difference between Podman and Docker and how Podman manages containers.](#difference-between-podman-and-docker-and-how-podman-manages-containers)

[How to run a rootless Podman container and how it functions.](#how-to-run-a-rootless-podman-container-and-how-it-functions)

[How Kubernetes runs containers and pods.](#how-kubernetes-runs-containers-and-pods)

[What are OCI, CRI, and CRI-O?](#what-are-oci-cri-and-cri-o)




## What are the basic components of Docker?


<p>Docker is defined as a freemium platform as a service (PaaS) solution that aids in creating, operating, and maintaining containers for isolated software development and testing by creating a virtualized operating system (OS) environment. </p>

## 8 Key Components of Docker.

<h4> 1. The Docker Engine </h4>

<li> Server: The Docker daemon (dockerd) is in charge of creating and managing containers. </li>
<li> Rest API: The Rest API enables the communication between applications and Docker and gives Dockerd instructions. </li>
<li> Command Line Interface (CLI): Docker commands are executed using the CLI. </li>


<h4> 2. Docker images </h4>

<h4> 3. Dockerfile </h4>

<h4> 4. The Docker Hub </h4>

<h4> 5. Docker volumes </h4>

<h4> 6. Docker Compose </h4>

<h4> 7. Docker Desktop </h4>

<h4> 8. Docker containers <h4>



## Difference between containerization and virtual machines.


<h4> Virtual machine </h4>

<li> Heavyweight </li>
<li> Limited performance </li>
<li> Each VM runs in its own OS. </li>
<li> Hardware-level virtualization </li>
<li> Startup time in mintues </li>
<li> Allocates required memory </li>
<li> Fully isolated and hence more secure </li>


<h4>Container </h4>

<li> Lightweight</li>
<li>Native performance </li>
<li> All containers share the host OS </li>
<li> OS virtualization</li>
<li>Startup time in milliseconds </li>
<li>Requires less memory space</li>
<li> Process-level isolation, possibly less secure</li>

 

## Why do we use containerization?

<p> Software developers use containerization to deploy applications in multiple environments without rewriting the program code. They build an application once and deploy it on multiple operating systems. For example, they run the same containers on Linux and Windows operating systems. </p>


## Difference between a container and a pod.

![](/pod.png)



## How Docker storage and networking work.



## What is runtime in containerization and what are the types in containerization?



## Difference between low-level and high-level runtime in containerization.



## Difference between Podman and Docker and how Podman manages containers.



## How to run a rootless Podman container and how it functions.
<p>
Customize how you run containers in Podman by changing the user namespace while in rootless mode. By default, rootless Podman containers map the user's user ID (UID) into the container as root of the user namespace.
</p>

<p> 
Customize how you run containers in Podman by changing the user namespace while in rootless mode. By default, rootless Podman containers map the user's user ID (UID) into the container as root of the user namespace. </p>

<p>
The basic syntax for running a command inside a container is: podman exec [options] [container-name] [command [args …]] The -ti option attached a virtual console and starts an interactive session </p>


## How Kubernetes runs containers and pods.
<p> 
Each node in a Kubernetes cluster runs the containers that form the Pods assigned to that node. Containers in a Pod are co-located and co-scheduled to run on the same node. </p>


## What are OCI, CRI, and CRI-O?

<h4>> OCI (Open Container Initiative): </h4>
<p>
<li> OCI is an open-source project that aims to create industry standards for container formats and runtime. </li>
<li> It defines two specifications: the Image Specification and the Runtime Specification. </li>
<li> Image Specification: Describes the format of the container image, including the filesystem layout and metadata. </li>
<li> Runtime Specification: Defines the requirements for a container runtime that can execute the container image. <li>
<li> OCI was established to ensure interoperability and portability across different container runtimes and platforms. </li>
</p>

<h4> CRI (Container Runtime Interface): </h4>
<p>

<li> CRI is a Kubernetes project that defines a standard interface between Kubernetes and container runtimes. </li>
<li> It allows Kubernetes to support different container runtimes without being tightly coupled to any specific implementation. </li>
<li> With CRI, Kubernetes components like kubelet can communicate with container runtimes via a standardized API.
CRI is designed to make it easier to integrate and switch  container runtimes within a Kubernetes cluster. </li> 

<h4> CRI-O: </h4>

<li> CRI-O is an implementation of the CRI that is lightweight and designed specifically for Kubernetes. </li>
<li> It is a container runtime that enables Kubernetes to directly interact with containers without the need for a full-fledged container orchestration platform. </li>
<li> CRI-O uses OCI-compliant container runtimes (such as runc) to create and run containers. </li>
<li> Unlike more comprehensive container runtimes like Docker, CRI-O focuses solely on the requirements of Kubernetes, making it simpler and more specialized. </li>
