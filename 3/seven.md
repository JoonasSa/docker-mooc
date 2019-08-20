# Kubernetes

Kubernetes is a container orchestration system that works on a higher level than Docker Compose.

Users of Kubernetes define their service architecture and Kubernetes takes care of the actual implementation.

## Why use Kubernetes?

Tools like Docker Compose make management and deployment of individual containers cumbersome when their numbers increase especially if they are running on different hosts. Often times development teams have to create custom pipelines and scripts to make their work easier. This sort of approach is very error prone and breaks easily if any changes are made.

Kubernetes doesn't just implement the specified architecture, it also makes managing, scaling, load balancing and distribution of containers a lot easier. It provides great logging functionality which is handy for debugging and monitoring the applications.

Kubernetes enables developers to create rolling updates for their services to achieve low down times when updates are pushed to production.

## When to use Kubernetes?

Kubernetes is useful when managing your teams contrainer orchestration becomes cumbersome and time consuming. Kubernetes makes devops work more agile and safer.

For smaller projects Kubernetes is most likely overkill and tools like Docker Compose should be used instead.

## Comparison to Docker Swarm

Docker Swarm is the high level container orchestration tool built for Docker. It turns a pool of containers into one virtual host.

Kubernetes supports higher traffic level and complexity of setup than Docker Swarm. Docker Swarm is a much simpler and faster tool to get started with.

In the end they are very similar and in only very big enterprise setups does it matter very much which one you use.
