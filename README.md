ECHO is on.
# Terraform S3 Static Website Hosting

This project automates the deployment of a static website using **Terraform** and **AWS S3**. It provisions an S3 bucket configured for static website hosting, uploads necessary files (HTML, CSS, and images), and sets up access controls to make the site publicly accessible.

---

## Table of Contents
- [Overview](#overview)
- [Project Structure](#projectstructure)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Usage](#usage)
- [Outputs](#outputs)

---

## Overview

This project includes:
- Creating an AWS S3 bucket to host static files.
- Uploading content such as:
  - `index.html`: Main webpage for the portfolio.
  - `error.html`: Custom error page.
  - `styles.css`: Stylesheet for design and animations.
  - `profile.png`: Profile picture used in the portfolio.
- Configuring static website settings:
  - `index.html` as the default document.
  - `error.html` for handling errors.

---

## Project Structure

- **`main.tf`**: Contains the Terraform configuration for creating resources.
- **`provider.tf`**: Interact with cloud services (AWS/Azure/GCP).
- **`variables.tf`**: Declares input variables (e.g., bucket name).
- **`Output.tf`**: Show information at terminal after the deployment

---

## Prerequisites

Ensure the following before running the Terraform script:
1. **AWS Account**:
   - Access to create and configure S3 buckets.
2. **Terraform**:
   - Install Terraform on your system: [Download Terraform](https://www.terraform.io/downloads).
3. **AWS CLI**:
   - Install the AWS CLI and configure it with your credentials.

---

## Setup

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/<your-username>/terraform-s3-static-website.git
   ```bash
   cd terraform-s3-static-website
2. Configure your AWS credentials using one of the following methods:
   ```bash
   aws configure
   ```bash
   export AWS_ACCESS_KEY_ID=<your-access-key>
   export AWS_SECRET_ACCESS_KEY=<your-secret-key>
3. Initialize Terraform in the project directory
   ```bash
   terraform init

---

## Usage

1. Plan the Infrastructure
   ```bash
   terraform plan
2. Apply the Configuration
   ```bash
   terraform apply

---

## Output
   
1. After deployment, Terraform will output the S3 website URL. Open the URL in your browser to view the static website.