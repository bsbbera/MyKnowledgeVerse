---
tags: [gcp, compute, vm, containers, serverless]
---

# GCP Compute Services

Google Cloud Platform offers a variety of compute services that allow you to run your applications in the cloud. These services range from infrastructure as a service (IaaS) to platform as a service (PaaS) and serverless computing options.

## Overview of Compute Services

GCP provides several compute options to meet different requirements:

1. [[Compute Engine|Compute Engine]] - Virtual machines (IaaS)
2. [[Google Kubernetes Engine|Google Kubernetes Engine (GKE)]] - Managed Kubernetes service
3. [[App Engine|App Engine]] - Fully managed application platform (PaaS)
4. [[Cloud Run|Cloud Run]] - Fully managed container platform
5. [[Cloud Functions|Cloud Functions]] - Serverless functions (FaaS)

## Comparison of GCP Compute Services

| Service | Type | Use Case | Management Overhead | Scalability |
|---------|------|----------|---------------------|-------------|
| Compute Engine | IaaS | Full control over infrastructure | High | Manual/Auto |
| GKE | Container Orchestration | Containerized applications | Medium | Auto |
| App Engine | PaaS | Web applications and services | Low | Auto |
| Cloud Run | Serverless Containers | Stateless containerized applications | Very Low | Auto |
| Cloud Functions | FaaS | Event-driven processing | Very Low | Auto |

## Choosing the Right Compute Service

When selecting a compute service, consider these factors:

- **Control vs. Convenience**: How much control do you need over the infrastructure?
- **Application Architecture**: Is your application monolithic or microservices-based?
- **Containerization**: Is your application containerized?
- **Scaling Requirements**: What are your scaling needs?
- **Management Overhead**: How much management overhead can you handle?
- **Cost Considerations**: What is your budget and cost model preference?

## Related Topics
- [[GCP Overview]]
- [[GCP Storage Services]]
- [[GCP Networking]]
- [[GCP Compute Pricing Models]]
