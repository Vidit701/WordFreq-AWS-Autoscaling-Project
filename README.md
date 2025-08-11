# WordFreq AWS Autoscaling Project

## Project Overview

This project demonstrates the design and implementation of a scalable word frequency analysis application using Amazon Web Services (AWS). The application processes large volumes of text data by leveraging AWS components such as EC2, S3, SQS, SNS, and Autoscaling Groups. Autoscaling policies dynamically adjust compute resources based on workload, optimizing cost and performance.

The original Go application code for word frequency analysis is not included in this repository due to licensing and intellectual property considerations.

## Repository Contents

- **Project Report**: A detailed document describing the system design, autoscaling setup, testing methodology, instance performance comparisons, and optimization strategies.
- **Sample Dataset**: A small collection of 10 text files representing a subset of the original data used for testing and demonstration purposes.
- **README.md**: This file, providing an overview and usage instructions.

## Architecture Summary

- **Compute Resources**: AWS EC2 instances (e.g., t3.medium) with autoscaling configured to respond to job queue workload.
- **Storage**: Two S3 buckets – one for uploading raw text files and another for processing.
- **Messaging**: SQS queues to handle job requests and results.
- **Notifications**: SNS topics for email alerts on processing status.
- **Monitoring & Autoscaling**: CloudWatch alarms monitor SQS queue length and trigger autoscaling actions based on predefined thresholds.
  
The autoscaling policies enable scaling up or down based on message volume, improving processing efficiency while controlling costs.

## Usage Notes

- This repository **does not contain the full application code** or AWS configuration scripts.
- To reproduce the system, users should:
  - Obtain or develop a compatible word frequency analysis application (e.g., in Go).
  - Set up corresponding AWS resources as described in the project report.
  - Upload text files to the provided sample data bucket or your own S3 bucket.
  - Configure autoscaling policies aligned with the queue metrics.

## Sample Dataset

The `sample-data/` directory contains 10 small text files that simulate the original dataset for testing purposes. These files can be uploaded to the designated AWS S3 bucket to start processing.

## Important Considerations

- AWS credentials and sensitive information are **not included** and should be managed securely by the user.
- The Go code is excluded to respect licensing restrictions.
- This project was completed using an AWS Academy sponsored account.

## References

- [AWS EC2 Autoscaling Documentation](https://aws.amazon.com/ec2/autoscaling/getting-started/)
- [AWS EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/)
- [AWS Pricing On-Demand Instances](https://aws.amazon.com/ec2/pricing/on-demand/)
- [AWS S3 Lifecycle Management](https://aws.amazon.com/s3/features/lifecycle/)
- [AWS Lambda and Serverless Architecture](https://aws.amazon.com/lambda/)
- [Naming Conventions for AWS Workloads](https://peritossolutions.com/aws/aws-workload-naming-convention/)

## Contact

For questions or further information, please contact [Your Name or Email].

---

