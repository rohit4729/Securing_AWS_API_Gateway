# 🔐 Securing AWS API Gateway with IAM Authentication

This project demonstrates how to **secure an AWS API Gateway endpoint** using **IAM user access keys** and integrate it with a **Lambda function**.  
It ensures that only authenticated users with valid AWS credentials can invoke the API.

---

## 🚀 Project Overview

1. **Lambda Function Setup**  
   - Created a simple Lambda function that returns a `"hello"` message.

2. **API Gateway Configuration**  
   - Created a new API with a resource named **`/demo_auth`**.  
   - Added a **GET method** and integrated it with the Lambda function.

3. **Enabling AWS IAM Authorization**  
   - In **Method Request** for the GET method, set the **Authorization Type → AWS_IAM**.  
   - This enforces that requests must be signed with IAM credentials.

4. **IAM User Creation**  
   - Created an **IAM user** with the policy:  
     - `AmazonAPIGatewayInvokeFullAccess`  
   - Generated **Access Key** and **Secret Key** for authentication.

5. **Secured API Invocation**  
   - Used the IAM credentials to send a **signed GET request** to the API Gateway endpoint.  
   - The Lambda function responds only when the request is authenticated.

---

## 🛠️ Tech Stack

- **AWS Lambda** → Serverless backend function  
- **AWS API Gateway** → API management & security  
- **AWS IAM** → Access control and authentication  

---

## 📌 Where we use it?
Answer:

1.This method is used when we want to secure your communicate among aws internal services. For example, EC2 <-->API Gateway

2. This is mostly used when you are using aws SDK.

## 🖼️ Screenshots :

<img width="1920" height="1080" alt="Screenshot (24)" src="https://github.com/user-attachments/assets/248264cc-360e-4558-99a5-45744d775df1" />
<img width="1920" height="1080" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/a1050a1e-c479-4b46-bb55-e81a03e41121" />
<img width="1920" height="1080" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/4a07f080-1ed1-4f03-967f-99acf0302d9e" />
<img width="1920" height="1080" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/3765a7fb-ab25-4341-a1d6-878025017678" />
<img width="1920" height="1080" alt="Screenshot (28)" src="https://github.com/user-attachments/assets/8816e577-2036-4986-b23b-cc9f368be7d8" />
<img width="1920" height="1080" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/6e6257a9-31a0-4dd4-a7ce-bb8efb8a30be" />
<img width="1920" height="1080" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/5cdb74ce-cd42-44a5-95b8-40a42c4ff590" />



