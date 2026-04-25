# Load-Balancer-project
AWS Application Load Balancer (ALB) Implementation


### Project Overview  :-
This project demonstrates how to implement an Application Load Balancer (ALB) in AWS to distribute traffic across multiple EC2 instances for high availability.

---

### Architecture :-
<img width="660" height="349" alt="LB Architecture" src="https://github.com/user-attachments/assets/27dd6a0a-7804-4f54-bfcb-6316d5662241" />


---

### Technologies Used :-

- AWS EC2  
- Application Load Balancer (ALB)  
- Target Groups  
- Apache Web Server  
- VPC & Subnets  

### Implementation Steps  

### Step 1 - EC2 Setup  :-
- Created two EC2 instances in same VPC
- Installed Apache web server on both instances
- Deployed different web content:
  - EC2-1 → "Hello!! I am Sujit Deshmukh"
  - EC2-2 → "Hey, I am Sujit. This is LB & AS Practical"

### Output : -  
**EC2 -1 -**
<img width="1917" height="222" alt="EC2-1-Output" src="https://github.com/user-attachments/assets/e52a4651-1eac-491e-b50e-6b1a1b5535d9" />  
**EC2 -2 -**
<img width="1917" height="251" alt="EC2-2-Output" src="https://github.com/user-attachments/assets/e3083bf7-2fbb-4fc8-aa7f-d98ab2725f46" />

---

### Step 2 - Target Group   :-
- Created target group with instance type
- Registered both EC2 instances
- Verified health check status (Healthy)

  <img width="1919" height="890" alt="TG" src="https://github.com/user-attachments/assets/c8804a0e-cfd2-47cf-bc64-c6321651a664" />


---

### Step 3 - Load Balancer Setup  :-
- Created Application Load Balancer (Internet-facing)
- Selected 2 subnets (different AZ)
- Configured HTTP listener (Port 80)
- Attached target group

<img width="1913" height="790" alt="LB" src="https://github.com/user-attachments/assets/bf98a67a-388d-4e4a-a34f-5992948862d9" />


---

### Step 4 - Testing Load Balancer  :-
- Accessed application using Load Balancer DNS
- Refreshed multiple times to verify traffic distribution

### Refresh 1:  
<img width="1919" height="193" alt="LB-Output-1" src="https://github.com/user-attachments/assets/4663ea05-0072-4428-a84a-64f527fecae8" />

### Refresh 2:  
<img width="1854" height="108" alt="LB-Output-2" src="https://github.com/user-attachments/assets/7262e977-c4f6-48f1-87f8-09e3cb1f6f80" />



---

### Verification  :-

- Load Balancer successfully distributed traffic across EC2 instances
- Different responses observed on refresh
- High availability validated by stopping one instance

---

### Output  :-

- Alternating responses between EC2-1 and EC2-2
- Successful failover when one instance stopped

---

### Learnings  :-

- Understanding of ALB and target groups
- Traffic distribution and health checks
- High availability architecture in AWS


