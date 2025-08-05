# Terraform-Zero-to-Hero-GCP-Edition

**Chapter 1: Getting Started with Terraform on GCP**

**Introduction to Terraform and Infrastructure as Code (IaC)**

In this session, we introduce the core concepts of Terraform and Infrastructure as Code (IaC). Understand how Terraform simplifies infrastructure provisioning and automation on Google Cloud Platform (GCP), making cloud resource management scalable, repeatable, and version-controlled.

**Installing Terraform on MacOS, Linux, and Windows**

Learn how to install Terraform across different operating systems. This section includes step-by-step instructions and verification commands to ensure a smooth setup experience, regardless of your platform.

**Setting up Terraform for GCP**

Dive into Google Cloud integration with Terraform. Learn how to authenticate using service accounts, configure the google provider, and prepare your environment to start provisioning GCP resources through Terraform.

**Writing Your First Terraform Code**

Start writing your first Terraform configuration. Understand the structure of .tf files, how to define GCP resources using HCL (HashiCorp Configuration Language), and run your first Terraform commands to provision infrastructure.

**Understanding the Terraform Lifecycle**

Explore the Terraform lifecycle in detail:

terraform init: Initialize a Terraform working directory.

terraform plan: Preview infrastructure changes before applying.

terraform apply: Apply the desired infrastructure state.

terraform destroy: Tear down resources.
Understand when and why to use each command in real-world scenarios.

**Launching a Compute Engine VM on GCP**

Level up your Terraform skills by provisioning a Compute Engine VM instance in GCP. Configure key attributes like machine type, zone, boot disk, and network settings.

**Chapter 2: Dynamic Configurations and Logic**

**Understanding GCP Providers and Resources**

Get deeper into how Terraform interacts with GCP through the Google provider. Understand how the provider block is used to authenticate and set the active project, region, and credentials. Learn the structure of GCP-specific resources like google_compute_instance, google_storage_bucket, and how each resource maps directly to a real-world GCP service.

**Leveraging Input Variables in GCP Projects**

Learn how to make Terraform configurations more dynamic and reusable using input variables. Customize project IDs, regions, VM sizes, and more without changing the code.

**Using Output Values to Extract Information**

Discover how to output important values like external IPs, instance names, and project IDs after applying your infrastructure — helpful for debugging and integration with other systems.

**Conditional Logic and Expressions**

Add logic to your Terraform code using conditional expressions. Apply different configurations based on environment types (e.g., dev vs prod) using count, for_each, and ternary conditions.

**Organizing and Formatting Your Codebase**

Follow best practices for clean and maintainable Terraform code. Use terraform fmt for formatting, terraform validate for correctness, and logical folder structures for large projects.
Chapter 3: Reusable Infrastructure and Modules

Building and Using Terraform Modules in GCP

Learn how to create modular Terraform configurations for your GCP infrastructure. Understand how to break down large configurations into reusable modules to manage Compute Engine, VPCs, IAM roles, and more. Organize your modules in directories and call them using the module block.

Simplifying Logic with Locals and Data Sources

Use local values to reduce repetition in your Terraform configurations. Explore data sources like google_compute_image or google_project to fetch information from existing GCP resources and incorporate them dynamically into your infrastructure.

Parameterizing Modules with Variables

Customize module behavior using input variables. Learn how to pass different values for different environments, projects, or regions when calling modules from your root configuration.

Accessing Module Outputs for Integration

Understand how to define outputs in your modules and access them in parent configurations. Use these outputs to pass information across modules or trigger dependent resources.

Discovering and Using the Terraform Module Registry

Explore the official Terraform Registry to find pre-built community modules for Google Cloud. Learn how to integrate and adapt these modules into your infrastructure securely and efficiently.

Chapter 4: Collaboration and State Management

Version Control for GCP Terraform Projects

Enhance team collaboration by managing your Terraform codebase with Git. Learn how to structure repositories, use branches, and commit changes effectively for GCP-based projects.

Protecting Secrets and Using .gitignore Wisely

Avoid exposing sensitive data like service account keys in version control. Use .gitignore to exclude secrets and leverage environment variables or Google Secret Manager for secure secret handling.

Introduction to Remote Backends

Understand how backends in Terraform help manage state files remotely. Explore the use of remote storage options to enable shared state management and collaboration.

Configuring GCS as a Backend for Terraform State

Learn how to configure Google Cloud Storage (GCS) as a remote backend for Terraform. Store state files securely in a bucket and ensure centralized access across teams.

Implementing State Locking with GCP

Prevent simultaneous changes to the infrastructure by using state locking. Explore how to implement locking mechanisms with GCS and Cloud Firestore or Bigtable to maintain consistency during collaboration.
Chapter 5: Provisioning and Configuration Actions

Customizing GCP Resources with Provisioners

Understand the purpose of provisioners in Terraform and how they allow you to execute scripts or commands on your Google Cloud resources. Learn when to use provisioners for post-creation setup or cleanup actions, and why they should be used cautiously.

Local-exec vs Remote-exec in GCP

Distinguish between local-exec and remote-exec provisioners. Use local-exec for triggering local scripts (e.g., Cloud Build triggers), and remote-exec to SSH into a GCE VM and run startup tasks like installing packages or configuring software.

Provisioners During Creation and Destruction

Explore how to configure provisioners to run during the creation (create) or destruction (destroy) phases of a GCP resource. Use this for tasks like registering with monitoring agents on creation or performing secure data cleanup before destruction.

Handling Errors and Failures in Provisioners

Learn about fault tolerance in provisioner execution. Use the on_failure argument to define fallback behavior, set retries and timeouts, and ensure that failures in scripts don’t leave your GCP infrastructure in an inconsistent state.
Chapter 6: Managing Environments with Workspaces

Introduction to GCP Workspaces with Terraform

Understand how Terraform workspaces help manage multiple environments like development, staging, and production in Google Cloud. Workspaces allow you to reuse the same configuration while maintaining isolated state files.

Creating and Switching Terraform Workspaces

Learn to create and manage workspaces using commands like terraform workspace new, select, and list. See how to use workspaces for environment segregation without duplicating your configuration files.

Environment Isolation and State Separation

Dive deeper into how workspaces help maintain different states for each environment. This enables teams to manage resources cleanly, avoid conflicts, and simplify lifecycle management for projects with multiple GCP deployments.
Chapter 7: Security 

Introduction to HashiCorp Vault for Secret Management

Get a high-level overview of HashiCorp Vault — a tool designed to securely store and manage secrets. Understand how Vault helps in protecting Terraform variables, credentials, and sensitive configuration values while provisioning resources on GCP.

Integrating Terraform with Vault on GCP

Learn how to use HashiCorp Vault as a secrets backend for your Terraform configurations. Discover how to fetch access tokens, credentials, or private data from Vault dynamically using the Vault provider, and apply these securely within your GCP infrastructure deployments.
