# ICE Cloud Security Lab

A hands-on cloud security lab built using Ubuntu, Docker, Docker Compose, MinIO, and Portainer.

The lab focuses on cloud object-storage security, access control, least privilege,
object versioning, application authentication, and storage security testing.

## 🎯 Objectives

- Configure MinIO as S3-compatible object storage
- Create users with restricted bucket access
- Implement least-privilege access control
- Create and attach custom storage policies
- Test read and write permissions
- Configure application access using Access Keys
- Enable and test object versioning
- Demonstrate object deletion and version recovery
- Test authorized and unauthorized storage access

## 🛠️ Technologies

- Ubuntu Linux
- Docker
- Docker Compose
- MinIO
- Portainer
- MinIO Client (mc)
- JSON Policies
- Git/GitHub

## 🔐 Security Concepts

### Least Privilege

A training user is created with access only to the required
`student-data` bucket and is restricted to read/write operations.

The user does not receive:

- User administration
- Bucket administration
- Finance data access
- Employee data access
- Server administration

## 🔑 Access Key Authentication

The lab demonstrates application authentication using:

- Access Key
- Secret Key
- Custom MinIO policy
- MinIO Client (`mc`)

The application account is restricted to the permissions required
for its operations.

## 🗂️ Object Versioning

Object versioning is enabled to demonstrate:

1. Upload Version 1
2. Modify the file
3. Upload Version 2
4. Upload Version 3
5. List object versions
6. Delete the object
7. Observe the delete marker
8. Restore an older version

This demonstrates how object versioning can help recover from
accidental deletion or modification.

## 🧪 Lab Testing

The lab includes testing of:

- Bucket access
- Read permissions
- Write permissions
- Restricted bucket access
- Application authentication
- Object versions
- Object deletion
- Version restoration

## 📁 Repository Structure

```text
ice-cloud-security-lab/
│
├── README.md
├── docker-compose.yml
├── .env.example
├── .gitignore
│
├── policies/
│   ├── student-policy.json
│   └── application-policy.json
│
├── docs/
│   └── minio-least-privilege-access-control-lab.md
│
└── screenshots/
