# Technical Questions

## Table of Contents

- [Architecture and Design Patterns](#architecture-and-design-patterns)
- [AWS and Serverless](#aws-and-serverless)
- [Debugging and Problem Solving](#debugging-and-problem-solving)
- [General Development Practices](#general-development-practices)

---

## Architecture and Design Patterns

### **1. How does the 3-Tier Architecture pattern work?**

<details>
<summary>Click to expand</summary>

The 3-Tier Architecture separates an application into three layers:

1. **Presentation Tier**: The front-end or user interface (UI) that interacts with the user.
2. **Logic Tier**: The back-end or business logic layer where data processing and application logic occur.
3. **Data Tier**: The database layer where data is stored and managed.

This separation helps organize code, making it more scalable, maintainable, and easier to manage.

</details>

---

### **2. How does the Hexagonal Architecture pattern work?**

<details>
<summary>Click to expand</summary>

Hexagonal Architecture separates the core business logic of an application from external systems (like databases or APIs).

- **Core**: The central business logic.
- **Ports**: Interfaces that allow external systems to communicate with the core.
- **Adapters**: Implementations that connect the core to external systems.

This makes the app easier to maintain, test, and adapt to new technologies.

</details>

---

### **3. How does the MVC pattern work?**

<details>
<summary>Click to expand</summary>

MVC (Model-View-Controller) splits an app into three parts:

1. **Model**: Manages data and business logic.
2. **View**: Displays data to the user.
3. **Controller**: Handles user input and updates the model or view.

This separation makes the code easier to manage and scale.

</details>

---

### **4. How does Clean Architecture work?**

<details>
<summary>Click to expand</summary>

Clean Architecture separates an application into layers to keep the core business logic independent of external factors. The layers are:

1. **Entities**: Core business models.
2. **Use Cases**: Application-specific logic.
3. **Interface Adapters**: Convert data between external systems (like UI or database) and core logic.
4. **Frameworks & Drivers**: External tools and frameworks.

This structure ensures flexibility, maintainability, and testability by keeping the core logic isolated from outside changes.

</details>

---

## AWS and Serverless

### **5. What is Node.js and why is it commonly used for backend development?**

<details>
<summary>Click to expand</summary>

Node.js is an open-source JavaScript runtime built on Chrome's V8 engine. It's widely used for backend development because it’s non-blocking and event-driven, which allows it to handle many requests simultaneously. This makes it ideal for real-time applications like chat apps or APIs that need to process many I/O operations without slowing down.

</details>

---

### **6. How does AWS Lambda work, and what are its main benefits?**

<details>
<summary>Click to expand</summary>

AWS Lambda is a serverless service that lets you run code without managing servers. You upload your code, and Lambda automatically handles scaling based on incoming requests. Its key benefits are:

- **Cost Efficiency**: You only pay for compute time.
- **Automatic Scaling**: It scales based on demand.
- **No Server Management**: No need to manage infrastructure.

Lambda is ideal for event-driven tasks like API requests, file uploads, or database triggers.

</details>

---

### **7. What is the best architecture for small Node.js applications using AWS?**

<details>
<summary>Click to expand</summary>

For small Node.js apps, a serverless architecture is often the best choice. Using AWS Lambda with API Gateway allows you to run code in response to HTTP requests without managing servers. This setup automatically scales based on traffic, and combined with services like DynamoDB for storage and S3 for files, it offers a cost-effective and low-maintenance solution ideal for small apps.

</details>

---

### **8. Why use Serverless? What are its advantages?**

<details>
<summary>Click to expand</summary>

Serverless eliminates infrastructure management, automatically scales with demand, and reduces costs by charging only for actual usage. It's ideal for building scalable, event-driven applications quickly, allowing developers to focus on writing code instead of managing servers.

</details>

---

## Debugging and Problem Solving

### **9. How do you approach debugging a complex issue?**

<details>
<summary>Click to expand</summary>

My process involves breaking the issue into smaller parts to isolate the root cause. I:

- Review logs and replicate the problem in a test environment.
- Use debugging tools and systematically test hypotheses until the issue is resolved.
</details>

---

### **10. What are the best approaches to resolve the typical timeout problem caused when a Lambda function triggered by API Gateway exceeds 30 seconds while managing large data, resulting in a 504 timeout?**

<details>
<summary>Click to expand</summary>

To avoid timeouts with large data in Lambda, use **SQS** or **Step Functions**:

- **SQS**: Send tasks to an SQS queue for asynchronous processing, avoiding API Gateway timeouts.
- **Step Functions**: Break the task into smaller steps, allowing multiple Lambdas to process data without hitting time limits.

Both methods prevent 504 timeouts by handling data processing in the background.

</details>

---

## General Development Practices

### **11. What is Infrastructure as Code (IaC)?**

<details>
<summary>Click to expand</summary>

Infrastructure as Code (IaC) is the practice of managing and provisioning infrastructure using code instead of manual processes. It allows developers to define servers, networks, databases, and other resources in configuration files, making deployments consistent, repeatable, and version-controlled. Tools like Terraform, AWS CloudFormation, and Ansible are commonly used for IaC.

</details>

---

### **12. How do you stay updated with the latest trends in technology?**

<details>
<summary>Click to expand</summary>

I follow top YouTubers, subscribe to blogs, and attend webinars to stay updated with the latest technology trends.

</details>

---

### **13. What is the best practice to manage a growing monolithic architecture with 1000+ files of code?**

<details>
<summary>Click to expand</summary>

The best approach is to shift to a **microservices architecture**, where the monolith is broken into smaller, independent services. This enhances scalability, maintainability, and resilience. Changes in one service don’t affect others, limiting issues to individual services and reducing system-wide downtime. You can update and deploy services independently without impacting the entire system.

</details>

---

### **14. What are the advantages of a monolithic architecture?**

<details>
<summary>Click to expand</summary>

Monolithic architecture is simpler to develop and test, especially for small applications. All components are in one codebase, so there's no need for complex inter-service communication. It's easier to debug and can be more efficient for smaller systems, as there’s less overhead.

</details>
