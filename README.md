# Serverless Cloud Dictionary Application

A serverless web application that allows users to search and retrieve cloud computing terminology.  
The project demonstrates how a frontend application can interact with a serverless backend using AWS services.

The application uses a REST API to retrieve definitions stored in a NoSQL database, showcasing a scalable and cost-efficient architecture.

---

## Architecture Overview

The application uses a fully serverless architecture, with the frontend communicating with backend services via an API.

Key AWS services used:

- AWS Amplify – Hosts the React frontend application
- Amazon API Gateway – Provides REST API endpoints
- AWS Lambda – Processes API requests
- Amazon DynamoDB – Stores cloud terms and definitions
- IAM Roles & Policies – Secures service access

---

## Architecture Diagram

<p align="center">
  <img src="https://i.gyazo.com/496518a98c9b47b98abf431c21cd230c.png" alt="Diagram" width="700">
  <br>
  <sub>Figure 1: Architecture Diagram</sub>
</p>

---

## Workflow

```text
User searches for cloud term
        ↓
Frontend hosted on Amplify
        ↓
Request sent to API Gateway
        ↓
API Gateway invokes Lambda function
        ↓
Lambda queries DynamoDB
        ↓
Definition returned to frontend
        ↓
Result displayed to the user
```

---

## Key AWS Configuration

Example infrastructure configurations used in the project.

<p align="center">
  <img src="https://i.gyazo.com/32dc03afd78b6bc6089eb4e2d4493f4e.png" alt="" width="700">
  <img src="https://i.gyazo.com/b0ee9d0d832067c32102f560205e6c4b.png" alt="API Gateway Endpoint" width="700">
  <br>
  <sub>Figure 2: API Gateway Endpoint</sub>
</p>

<p align="center">
  <img src="https://i.gyazo.com/d6ebe4f8856bb4e6db56399f422cbf1c.png" alt="DynamoDB Table" width="700">
  <br>
  <sub>Figure 3: DynamoDB Table</sub>
</p>

---

## Application Interface

Example of the dictionary search interface and returned definition.

<p align="center">
  <img src="https://i.gyazo.com/af1fdb2dbefa0f128a1ee88409170f44.png" alt="Dictionary Search UI" width="700">
  <br>
  <sub>Figure 4: Dictionary Search UI</sub>
</p>

---

## Future Improvements

- Allow users to submit new terms
- Implement caching for faster lookups
- Add authentication for user contributions
- Expand the dictionary dataset

---

## Local Development

This frontend application was bootstrapped using Create React App.

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm start
```

The application will run at:

```
http://localhost:3000
```

Build the production version:

```bash
npm run build
```

---

## Deployment

The application is deployed using AWS Amplify for frontend hosting and continuous deployment.
