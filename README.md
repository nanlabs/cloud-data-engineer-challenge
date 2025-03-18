# 🚀 Cloud Data Engineer Challenge

Welcome to the **Cloud Data Engineer Challenge!** 🎉 This challenge is designed to evaluate your ability to work with **Infrastructure as Code (IaC), AWS data services, and data engineering workflows**, ensuring efficient data ingestion, storage, and querying.

> [!NOTE]
> You can use **any IaC tool of your choice** (Terraform preferred, but alternatives are allowed). If you choose a different tool or a combination of tools, **justify your decision!**

## ⚡ Challenge Overview

Your task is to deploy the following infrastructure on AWS:

> 🎯 **Key Objectives:**

- **An S3 bucket** that will receive data files as new objects.
- **A Lambda function** that is triggered by a `PUT` event in the S3 bucket.
- **The Lambda function must:**
  - Process the ingested data and perform a minimal aggregation.
  - Store the processed data in a **PostgreSQL database with PostGIS enabled**.
  - Expose an API Gateway endpoint (`GET /aggregated-data`) to query and retrieve the aggregated data.
- **A PostgreSQL database** running in a private subnet with PostGIS enabled.
- **Networking must include:** VPC, public/private subnets, and security groups.
- **The Lambda must be in a private subnet** and use a NAT Gateway in a public subnet for internet access 🌍
- **CloudWatch logs** should capture Lambda execution details and possible errors.

> [!IMPORTANT]
> Ensure that your solution is modular, well-documented, and follows best practices for security and maintainability.

## 📌 Requirements

### 🛠 Tech Stack

> ⚡ **Must Include:**

- **IaC:** Any tool of your choice (**Terraform preferred**, but others are allowed if justified).
- **AWS Services:** S3, Lambda, API Gateway, CloudWatch, PostgreSQL with PostGIS (RDS or self-hosted on EC2).
- **CI/CD:** GitHub Actions for automation 🏗
- **Code Quality:** Pre-commit hooks for linting and security checks 🛡

### 📄 Expected Deliverables

> 📥 **Your submission must be a Pull Request that includes:**

- **An IaC module** that deploys the entire architecture.
- **A `README.md`** with deployment instructions and tool selection justification.
- **A working API Gateway endpoint** that returns the aggregated data stored in PostgreSQL.
- **CloudWatch logs** capturing Lambda execution details.

> [!TIP]
> Use the `docs` folder to store any additional documentation or diagrams that help explain your solution.
> Mention any assumptions or constraints in your `README.md`.

## 🌟 Nice to Have

> 💡 **Bonus Points For:**

- **GitHub Actions to validate IaC** (e.g., `terraform fmt`, `terraform validate`, or equivalent for chosen tool).
- **Pre-commit hooks** to ensure linting and formatting checks before commits.
- **Tests for your IaC code** using `terraform validate`, `Terratest`, or equivalent for chosen tool.
- **Monitoring alerts** (e.g., AWS CloudWatch Alarms for Lambda errors).
- **Docker or Docker Compose** to facilitate local testing, such as:
  - Running a local PostgreSQL database with PostGIS to simulate the cloud environment 🛠
  - Providing a local S3-compatible service (e.g., MinIO) to test file ingestion before deployment 🖥

> [!TIP]
> Looking for inspiration or additional ideas to earn extra points? Check out our **[Awesome NaNLABS repository](https://github.com/nanlabs/awesome-nan)** for reference projects and best practices! 🚀

## 📥 Submission Guidelines

> 📌 **Follow these steps to submit your solution:**

1. **Fork this repository.**
2. **Create a feature branch** for your implementation.
3. **Commit your changes** with meaningful commit messages.
4. **Open a Pull Request** following the provided template.
5. **Our team will review** and provide feedback.

## ✅ Evaluation Criteria

> 🔍 **What we'll be looking at:**

- **Correctness and completeness** of the solution.
- **Code quality, modularity, and best practices.**
- **Security considerations** in networking and IAM roles.
- **Justification for chosen tool(s).**
- **Documentation clarity.**
- **Bonus points for additional features.**

## 🎯 **Good luck and happy coding!** 🚀
