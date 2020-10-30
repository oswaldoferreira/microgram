# microgram
A instagram-like application split into microservices.

### Setup

Follow the instructions for each repo to run all services within Docker or local environment.

- https://github.com/oswaldoferreira/microgram-auth
- https://github.com/oswaldoferreira/microgram-feed
- https://github.com/oswaldoferreira/microgram-fe

By the end you should have the following containers running locally:

```bash
› docker ps
CONTAINER ID        IMAGE                   COMMAND                  CREATED              STATUS              PORTS                    NAMES
ad7bad56e9ca        microgram-feed:latest   "docker-entrypoint.s…"   About a minute ago   Up About a minute   0.0.0.0:8080->8080/tcp   loving_turing
26530617d31c        microgram-auth:latest   "docker-entrypoint.s…"   About a minute ago   Up About a minute   0.0.0.0:5000->5000/tcp   sad_swanson
9aa6b98d7bb7        microgram-fe:latest     "/docker-entrypoint.…"   About an hour ago    Up About an hour    0.0.0.0:4200->80/tcp     hungry_lumiere
```

The `microgram-fe` (SPA) can be accessed at port `4200`.

```bash
› curl -I localhost:4200
HTTP/1.1 200 OK
Server: nginx/1.19.3
Date: Fri, 30 Oct 2020 01:34:24 GMT
Content-Type: text/html
Content-Length: 995
Last-Modified: Thu, 29 Oct 2020 20:52:14 GMT
Connection: keep-alive
ETag: "5f9b2b7e-3e3"
Accept-Ranges: bytes
```

### Deployment

The repositories above fall short when describing the processes to setup a Kubernetes cluster, but, it provides the YML files that you'll need once you get it running. 

I recommend taking a further look at [GKE](https://cloud.google.com/kubernetes-engine) and [EKS](https://aws.amazon.com/pt/eks/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc&eks-blogs.sort-by=item.additionalFields.createdDate&eks-blogs.sort-order=desc) solutions.

### Architecture



