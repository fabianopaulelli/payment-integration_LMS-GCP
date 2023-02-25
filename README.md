# 
`#RRGGBB` The background color should be `#ffffff` for light mode and `#0d1117` for dark mode.


  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">

# **Integration between a Payment System and an LMS - A real-time solution using GCP**

## **Overview**
This is a freela where a client wanted to change their e-Learning platform to an LMS (Learning Management System). In general, e-Learning and LMS have the same purpose: to offer an environment to place course content (videos, audio, text, etc.), but the LMS has some extra resources, like gamification. So they wanted me to integrate these two platforms, where the LMS will be the new course content platform, and the e-Learning platform will act as the payment system and the course catalog.

> So, the idea here is to create a fictitious scenario based on this project, where a client asks to use GCP (Google Cloud Platform) to integrate these two platforms, which should be real-time, and we have to create a relational database using BigQuery to feed a dashboard to track revenue.




## **Introduction**
This is a project where a company, besides other services, created and provided specialized courses in an e-Learning platform for their target public. But in a moment in the past, they realized that they needed more than just a platform that provided courses. They wanted to have a platform that could track their student's progress, offer conclusion certificates, and other features that an e-Learning platform couldn't provide. So they decided to migrate to an LMS (Learning Management System), but at the same time, they still wanted to stick with the e-Learning platform to showcase the courses catalogs and the payment system.

#### **Previous Architecture**
<picture>
<img src="./img/architecture_1.drawio.svg">
  <figcaption>test caption</figcaption>
</picture>

#### **New Architecture**

#### **Overview**
In this new architecture, we have detached the LMS from the payment system. The LMS and the payment system are now standalone services independent of each other. We could go even further by detaching the course catalog, and then we would have 3 independent systems. 

> **_Note:_** By saying payment system, actually, I'm referring to the old LMS that provided the course catalog, the LMS itself, and the payment system. But I pointed as a payment system because we can now use any payment system as we want and attach it to the new LMS.

[![](./img/architecture_2.drawio.svg)](#New-Architecture)


## **Objective**
Set up an integration between the new LMS and the old e-Learning platform, so that they could communicate with each other without any impact on the clients/students as well providing a better learning environment for the students.

## **Tech Stack**
We're going to use Google Cloud to build up this integration. So we need a NoSQL database to store the student data as expiration time, 

|  | GCP Stack  | 
| --- | --- |
| [![](./img/firestore.svg)](#New-Architecture) | Google Firestore |
| [![](./img/cloud_functions.svg)](#New-Architecture) | Google Cloud Function |
| [![](./img/pubsub.svg)](#New-Architecture) | Google Cloud Pub/Sub |


- Webhook
