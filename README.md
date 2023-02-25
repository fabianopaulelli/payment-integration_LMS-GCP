# **Integration between a Payment System and an LMS - A real-time solution using GCP**

## **Overview**
This is a real freela where a client wanted to change their e-Learning platform to an LMS (Learning Management System). In general, e-Learning and LMS have the same purpose: to offer an environment to place course content (videos, audio, text, etc.), but the LMS has some extra resources, like gamification and so on. So they wanted me to integrate these two platforms, where the LMS will be the new course content platform, and the e-Learning platform will act as the payment system and the course catalog.


> So, the idea here is to create a fictitious scenario based on this real project, where a client will allow us to use GCP (Google Cloud Platform) to integrate these two platforms, which should be real-time and create a relational database using BigQuery to feed a dashboard to track revenue. We're going to work with these skills in this project: 
> - Data Architect: By designing the architecture of the integration using GCP
> - Data Engineer: By implementing the architecture designed, setup a NoSQL database, a data warehouse and works with the streaming data
> - Data Analyst: By creating a dashboard to track the revenue of the courses

## **Tech Stack**
We're going to use Google Cloud to build up this integration. So we need a NoSQL database to store the student data as expiration time, 

|  | GCP Stack  | 
| --- | --- |
| <picture><img src="./img/firestore.svg"></picture> | Google Firestore |
| <picture><img src="./img/cloud_functions.svg"></picture> | Google Cloud Function |
| <picture><img src="./img/pubsub.svg"></picture> | Google Cloud Pub/Sub |


- Webhook