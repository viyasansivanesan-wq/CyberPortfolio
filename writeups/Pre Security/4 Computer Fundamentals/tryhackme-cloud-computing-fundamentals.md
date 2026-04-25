TryHackMe — Cloud Computing Fundamentals

Platform: TryHackMe

Room: Cloud Computing Fundamentals

Difficulty: Easy

Category: Cybersecurity 101 / Computing Fundamentals

Date Completed: April 2026

Status: ✅ Completed



Overview

Completed the Cloud Computing Fundamentals room on TryHackMe. This room introduces cloud computing — what it is, the different deployment models, the three main service models (IaaS, PaaS, SaaS), and key characteristics like scalability. Ends with a practical task simulating cloud resource deployment and cost calculation in a simulated AWS-style environment.



Objectives



Understand what cloud computing is and why it's used

Learn the three cloud deployment models (Public, Private, Hybrid)

Understand the three cloud service models (IaaS, PaaS, SaaS)

Learn key cloud characteristics including scalability and elasticity

Complete a practical cloud environment cost calculation task





Key Concepts

What is Cloud Computing?

Cloud computing delivers computing resources (servers, storage, networking, software) over the internet on demand. Instead of owning physical infrastructure, organisations rent resources from cloud providers like AWS, Azure, or Google Cloud — paying only for what they use.



Cloud Deployment Models

ModelDescriptionPublic CloudResources hosted by a third-party provider, shared across multiple customers — the most common deployment typePrivate CloudResources dedicated to a single organisation, hosted on-premises or by a providerHybrid CloudCombination of public and private cloud, allowing data and apps to move between them



Cloud Service Models

ModelFull NameDescriptionResponsibilityIaaSInfrastructure as a ServiceProvides raw compute, storage, and networkingCustomer manages OS and abovePaaSPlatform as a ServiceProvides a platform for application development — infrastructure handled by providerCustomer focuses only on app developmentSaaSSoftware as a ServiceFully managed software delivered via browserCustomer just uses the application



PaaS is the best choice when you want to deploy an application to the internet while leaving all infrastructure management to the provider.





Key Cloud Characteristics



Scalability — the ability to handle unexpected increases in traffic or demand by expanding resources

Elasticity — automatically scaling resources up or down based on current demand

On-demand self-service — provision resources without needing human intervention from the provider

Pay-as-you-go — only pay for what you actually use





Practical Task — Cloud Cost Calculator

Used a simulated cloud environment (AWS-style EC2 instances) to deploy resources and calculate running costs in credits.

ScenarioAnswerTotal cost if study-machine-1 and study-machine-2 are stopped30 creditsMonthly cost of an m5.large EC2 instance70 creditsTotal cost if only the new instances are running150 creditsTotal cost of entire environment with a third t3a.small study machine added188 credits



Questions \& Answers

QuestionAnswerWhat characteristic handles unexpected increases in access?ScalabilityWhat is the most common type of cloud deployment?Public CloudBest cloud service for app development, leaving infrastructure to others?PaaSTotal cost if study-machine-1 and study-machine-2 are stopped30Monthly credits for an m5.large EC2 instance70Total cost if only new instances are running150Total cost with a third t3a.small study machine added188



What I Learned

Cloud computing is now the default infrastructure model for most organisations, which makes it a critical area for cybersecurity. Misconfigurations in cloud environments (exposed S3 buckets, overly permissive IAM roles, public-facing instances) are among the most common real-world vulnerabilities. Understanding the service models is important for knowing where responsibility lies — in IaaS the customer is responsible for securing the OS and above, while in SaaS the provider handles almost everything. The cost calculation task gave practical insight into how cloud billing works, which is relevant for understanding cloud architecture decisions.



Challenges

No major technical challenges. The cost calculation task required reading the instance pricing table carefully and applying basic arithmetic across multiple scenarios.



Takeaways



Cloud computing delivers on-demand infrastructure over the internet — pay only for what you use

Public cloud is the most common deployment model

IaaS, PaaS, and SaaS differ in how much responsibility shifts to the provider

Scalability is the key cloud feature for handling unexpected traffic spikes

Cloud misconfiguration is one of the most common real-world security vulnerabilities — critical area for pentesting





Next Steps



Continue with the Cybersecurity 101 pathway

Explore AWS/Azure security fundamentals

Look into common cloud misconfigurations (S3 bucket exposure, IAM privilege escalation)

