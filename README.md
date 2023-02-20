# **Documentation**

### **Previous Architecture**

[![](./img/architecture_1.drawio.svg)](#Previous-Architecture)


### **New Architecture**

#### **Overview**
In this new architecture, we have detached the LMS from the payment system. The LMS and the payment system are now standalone services independent of each other. We could go even further by detaching the course catalog, and then we would have 3 independent systems. 

> **_Note:_** By saying payment system, actually, I'm referring to the old LMS that provided the course catalog, the LMS itself, and the payment system. But I pointed as a payment system because we can now use any payment system as we want and attach it to the new LMS.

[![](./img/architecture_2.drawio.svg)](#New-Architecture)
