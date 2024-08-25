# VPC Endpoint with S3 Access

## Description
This project demonstrates how to create a VPC Endpoint for S3 and configure it to allow access only from within a specific VPC. We'll use an EC2 instance to test the endpoint's availability and verify that the S3 bucket is accessible only via the VPC Endpoint.

![image](https://github.com/user-attachments/assets/b3831668-a733-41b9-b97b-e6e62810dcc2)



## Steps Overview

### 1. Create a VPC
- **Description:** A Virtual Private Cloud (VPC) was created to serve as a network environment where resources can be isolated.

### 2. Create a Subnet
- **Description:** A subnet was created within the VPC to host resources such as EC2 instances.

### 3. Attach an Internet Gateway
- **Description:** An Internet Gateway was created and attached to the VPC, providing internet access to resources within the subnet.

### 4. Create a VPC Endpoint for S3
- **Description:** A VPC Endpoint was created within the VPC and linked to the subnet, allowing private connectivity to the S3 service without using an Internet Gateway or NAT device.

### 5. Set Endpoint Permissions
- **Description:** The VPC Endpoint was configured with full access permissions to S3, enabling unrestricted operations on S3 resources within the VPC.

### 6. Launch an EC2 Instance
- **Description:** An EC2 instance was launched in the subnet and assigned an IAM role with S3 full access permissions to interact with the S3 service.

### 7. Test Endpoint Connectivity
- **Description:** A connection test was conducted from the EC2 instance to confirm that access to S3 was routed through the VPC Endpoint.

### 8. Apply S3 Bucket Policy
- **Description:** A bucket policy was applied to restrict access to the S3 bucket, ensuring that only requests coming from the VPC Endpoint were allowed.

### 9. Test Access from a Different VPC
- **Description:** An access test was performed from an EC2 instance in a different VPC to verify that the bucket is not accessible without routing through the designated VPC Endpoint.


## Conclusion
By following these steps, you have successfully secured S3 access within your VPC, ensuring that no external entities can access your S3 bucket unless they are operating within the specified VPC.

