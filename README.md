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

## 📌 Example API Invocation

You can test the secured API using the **AWS CLI**:

```bash
aws apigateway test-invoke-method \
  --rest-api-id <your-api-id> \
  --resource-id <your-resource-id> \
  --http-method GET \
  --region <your-region> \
  --profile <your-iam-user-profile>

