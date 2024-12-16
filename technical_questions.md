# Technical Questions

## Table of Contents

<details>
  <summary>1. Architecture and Design Patterns (4)</summary>

- [1.1. How does the 3-Tier Architecture pattern work?](#11-how-does-the-3-tier-architecture-pattern-work)
- [1.2. How does the Hexagonal Architecture pattern work?](#12-how-does-the-hexagonal-architecture-pattern-work)
- [1.3. How does the MVC pattern work?](#13-how-does-the-mvc-pattern-work)
- [1.4. How does Clean Architecture work?](#14-how-does-clean-architecture-work)

</details>

<details>
  <summary>2. AWS and Serverless (4)</summary>

- [2.1. What is Node.js and why is it commonly used for backend development?](#21-what-is-nodejs-and-why-is-it-commonly-used-for-backend-development)
- [2.2. How does AWS Lambda work, and what are its main benefits?](#22-how-does-aws-lambda-work-and-what-are-its-main-benefits)
- [2.3. What is the best architecture for small Node.js applications using AWS?](#23-what-is-the-best-architecture-for-small-nodejs-applications-using-aws)
- [2.4. Why use Serverless? What are its advantages?](#24-why-use-serverless-what-are-its-advantages)

</details>

<details>
  <summary>3. Debugging and Problem Solving (2)</summary>

- [3.1. How do you approach debugging a complex issue?](#31-how-do-you-approach-debugging-a-complex-issue)
- [3.2. What are the best approaches to resolve the typical timeout problem caused when a Lambda function triggered by API Gateway exceeds 30 seconds while managing large data, resulting in a 504 timeout?](#32-what-are-the-best-approaches-to-resolve-the-typical-timeout-problem-caused-when-a-lambda-function-triggered-by-api-gateway-exceeds-30-seconds-while-managing-large-data-resulting-in-a-504-timeout)

</details>

<details>
  <summary>4. General Development Practices (10)</summary>

- [4.1. What is Infrastructure as Code (IaC)?](#41-what-is-infrastructure-as-code-iac)
- [4.2. How do you stay updated with the latest trends in technology?](#42-how-do-you-stay-updated-with-the-latest-trends-in-technology)
- [4.3. What is the best practice to manage a growing monolithic architecture with 1000+ files of code?](#43-what-is-the-best-practice-to-manage-a-growing-monolithic-architecture-with-1000-files-of-code)
- [4.4. What are the advantages of a monolithic architecture?](#44-what-are-the-advantages-of-a-monolithic-architecture)
- [4.5. What is a REST API?](#45-what-is-a-rest-api)
- [4.6. What is a SOAP API?](#46-what-is-a-soap-api)
- [4.7. What is GraphQL?](#47-what-is-graphql)
- [4.8. What is the difference between SQL and NoSQL?](#48-what-is-the-difference-between-sql-and-nosql)
- [4.9. What is CI/CD and its advantages?](#49-what-is-cicd-and-its-advantages)
- [4.10. What is the difference between TypeScript and JavaScript?](#410-what-is-the-difference-between-typescript-and-javascript)

</details>

---

## 1. Architecture and Design Patterns

### 1.1. How does the 3-Tier Architecture pattern work?

<details>
<summary>Click to expand</summary>

The 3-Tier Architecture separates an application into three layers:

1. Presentation Tier: The front-end or user interface (UI) that interacts with the user.
2. Logic Tier: The back-end or business logic layer where data processing and application logic occur.
3. Data Tier: The database layer where data is stored and managed.

This separation helps organize code, making it more scalable, maintainable, and easier to manage.

</details>

---

### 1.2. How does the Hexagonal Architecture pattern work?

<details>
<summary>Click to expand</summary>

Hexagonal Architecture separates the core business logic of an application from external systems (like databases or APIs).

- Core: The central business logic.
- Ports: Interfaces that allow external systems to communicate with the core.
- Adapters: Implementations that connect the core to external systems.

This makes the app easier to maintain, test, and adapt to new technologies.

</details>

---

### 1.3. How does the MVC pattern work?

<details>
<summary>Click to expand</summary>

MVC (Model-View-Controller) splits an app into three parts:

1. Model: Manages data and business logic.
2. View: Displays data to the user.
3. Controller: Handles user input and updates the model or view.

This separation makes the code easier to manage and scale.

</details>

---

### 1.4. How does Clean Architecture work?

<details>
<summary>Click to expand</summary>

Clean Architecture separates an application into layers to keep the core business logic independent of external factors. The layers are:

1. Entities: Core business models.
2. Use Cases: Application-specific logic.
3. Interface Adapters: Convert data between external systems (like UI or database) and core logic.
4. Frameworks & Drivers: External tools and frameworks.

This structure ensures flexibility, maintainability, and testability by keeping the core logic isolated from outside changes.

</details>

---

## 2. AWS and Serverless

### 2.1. What is Node.js and why is it commonly used for backend development?

<details>
<summary>Click to expand</summary>

Node.js is an open-source JavaScript runtime built on Chrome's V8 engine. It's widely used for backend development because it’s non-blocking and event-driven, which allows it to handle many requests simultaneously. This makes it ideal for real-time applications like chat apps or APIs that need to process many I/O operations without slowing down.

</details>

---

### 2.2. How does AWS Lambda work, and what are its main benefits?

<details>
<summary>Click to expand</summary>

AWS Lambda is a serverless service that lets you run code without managing servers. You upload your code, and Lambda automatically handles scaling based on incoming requests. Its key benefits are:

- Cost Efficiency: You only pay for compute time.
- Automatic Scaling: It scales based on demand.
- No Server Management: No need to manage infrastructure.

Lambda is ideal for event-driven tasks like API requests, file uploads, or database triggers.

</details>

---

### 2.3. What is the best architecture for small Node.js applications using AWS?

<details>
<summary>Click to expand</summary>

For small Node.js apps, a serverless architecture is often the best choice. Using AWS Lambda with API Gateway allows you to run code in response to HTTP requests without managing servers. This setup automatically scales based on traffic, and combined with services like DynamoDB for storage and S3 for files, it offers a cost-effective and low-maintenance solution ideal for small apps.

</details>

---

### 2.4. Why use Serverless? What are its advantages?

<details>
<summary>Click to expand</summary>

Serverless eliminates infrastructure management, automatically scales with demand, and reduces costs by charging only for actual usage. It's ideal for building scalable, event-driven applications quickly, allowing developers to focus on writing code instead of managing servers.

</details>

---

## 3. Debugging and Problem Solving

### 3.1. How do you approach debugging a complex issue?

<details>
<summary>Click to expand</summary>

My process involves breaking the issue into smaller parts to isolate the root cause. I:

- Review logs and replicate the problem in a test environment.
- Use debugging tools and systematically test hypotheses until the issue is resolved.
</details>

---

### 3.2. What are the best approaches to resolve the typical timeout problem caused when a Lambda function triggered by API Gateway exceeds 30 seconds while managing large data, resulting in a 504 timeout?

<details>
<summary>Click to expand</summary>

To avoid timeouts with large data in Lambda, use SQS or Step Functions:

- SQS: Send tasks to an SQS queue for asynchronous processing, avoiding API Gateway timeouts.
- Step Functions: Break the task into smaller steps, allowing multiple Lambdas to process data without hitting time limits.

Both methods prevent 504 timeouts by handling data processing in the background.

</details>

---

## 4. General Development Practices

### 4.1. What is Infrastructure as Code (IaC)?

<details>
<summary>Click to expand</summary>

Infrastructure as Code (IaC) is the practice of managing and provisioning infrastructure using code instead of manual processes. It allows developers to define servers, networks, databases, and other resources in configuration files, making deployments consistent, repeatable, and version-controlled. Tools like Terraform, AWS CloudFormation, and Ansible are commonly used for IaC.

</details>

---

### 4.2. How do you stay updated with the latest trends in technology?

<details>
<summary>Click to expand</summary>

I follow top YouTubers, subscribe to blogs, and attend webinars to stay updated with the latest technology trends.

</details>

---

### 4.3. What is the best practice to manage a growing monolithic architecture with 1000+ files of code?

<details>
<summary>Click to expand</summary>

The best approach is to shift to a microservices architecture, where the monolith is broken into smaller, independent services. This enhances scalability, maintainability, and resilience. Changes in one service don’t affect others, limiting issues to individual services and reducing system-wide downtime. You can update and deploy services independently without impacting the entire system.

</details>

---

### 4.4. What are the advantages of a monolithic architecture?

<details>
<summary>Click to expand</summary>

Monolithic architecture is simpler to develop and test, especially for small applications. All components are in one codebase, so there's no need for complex inter-service communication. It's easier to debug and can be more efficient for smaller systems, as there’s less overhead.

</details>

---

### 4.5. What is a REST API?

<details>
<summary>Click to expand</summary>

A REST API uses HTTP methods (GET, POST, PUT, DELETE) to allow communication between clients and servers. It is stateless, meaning each request is independent, and is known for its simplicity, scalability, and flexibility.

</details>

---

### 4.6. What is a SOAP API?

<details>
<summary>Click to expand</summary>

A SOAP API is a protocol for exchanging structured information using XML over HTTP, SMTP, or other transport protocols. It enforces strict standards for security and error handling, making it reliable for enterprise use.

</details>

---

### 4.7. What is GraphQL?

<details>
<summary>Click to expand</summary>

GraphQL is a query language for APIs that allows clients to request exactly the data they need. Unlike REST, it uses a single endpoint and reduces data over-fetching and under-fetching.

</details>

---

### 4.8. What is the difference between SQL and NoSQL?

<details>
<summary>Click to expand</summary>

- SQL: Relational databases with structured tables and predefined schemas (e.g., MySQL, PostgreSQL).
- NoSQL: Non-relational databases with flexible formats, ideal for unstructured data and scalability (e.g., MongoDB, DynamoDB).

</details>

---

### 4.9. What is CI/CD and its advantages?

<details>
<summary>Click to expand</summary>

CI/CD automates code integration, testing, and deployment.

- Continuous Integration: Regularly merges code with automated tests.
- Continuous Deployment: Automatically deploys approved changes.

Advantages:

- Faster delivery.
- Fewer errors through automation.
- Quick feedback and iteration.

</details>

---

### 4.10. What is the difference between TypeScript and JavaScript?

<details>
<summary>Click to expand</summary>

- JavaScript: Dynamic, loosely typed, used for web development.
- TypeScript: Adds static typing for error prevention, compiles to JavaScript, and is better for large projects.

</details>
