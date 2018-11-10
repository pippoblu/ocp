# Homework Assignment
## Goals
Assess hands-on proficiency with Red Hat OpenShift Container Platform Deployment advanced topics
Complete course leading to Red Hat Delivery Specialist – Advanced Platform-as-a-Service accreditation

## Criteria
Assignments should take the average student 30-40 hours to complete
Assignments are an individual effort
Each student completes his or her own assignment without collaboration
Assignments should simulate a challenge typically encountered in a Red Hat Consulting engagement
Assignment requirements are intentionally a bit vague

Grading is as follows:

20% : Basic Requirements section
20% : HA Deployment section
20% : Environment Configuration section
20% : CICD Workflow section
20% : Multitenancy section

Provide sufficient documentation for each section
Sections without documentation will not be graded

# 1. Business Use Case
You are a consultant assigned to a telecommunications company called MitziCom. MitziCom provides hosting and cloud services to a variety of clients, from medium size companies to enterprise giants.

MitziCom has asked you to lead a 30-40 hour proof-of-concept (POC) using Red Hat OpenShift Container Platform. The purpose of the POC is to determine the feasibility of using Red Hat OpenShift Container Platform as a target for internal and client workloads.

# 2. POC Requirements
MitziCom management requires that you include all of the items listed in these subsections in your POC.

## 2.1. Basic Requirements
Ability to authenticate at the master console
Registry has storage attached and working
Router is configured on each infranode
PVs of different types are available for users to consume
Ability to deploy a simple app (nodejs-mongo-persistent)

## 2.2. HA Deployment
There are three masters working
There are three etcd instances working
There is a load balancer to access the masters
There is a load balancer/DNS for both infranodes
There are at least two infranodes

## 2.3. Environment Configuration
NetworkPolicy is configured and working with default project isolation (simulate Multitenancy)
Aggregated logging is configured and working
Metrics collection is configured and working
Router and Registry Pods run on Infranodes
Metrics and Logging components run on Infranodes

## 2.4. CICD Workflow
Jenkins pod is running with a persistent volume
Jenkins deploys openshift-tasks app
Jenkins OpenShift plugin is used to create a CICD workflow
HPA is configured and working on production deployment of openshift-tasks

## 2.5. Multitenancy
Multiple clients/customers created
Dedicated node for each client/customer
admissionControl plugin sets specific limits per label (client/customer)
The new project template is modified so that it includes a LimitRange
The new user template is used to create a user object with the specific label value
On-boarding new client documentation explains how to create a new client/customer
