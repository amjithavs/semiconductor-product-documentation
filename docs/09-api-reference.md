# API Reference

## Overview

The Enterprise Test Platform REST API enables applications to automate project management, validation workflows, report generation, and system administration.

---

# Base URL

```text
https://api.enterprise-platform.com/v1
```

---

# Authentication

All API requests require a Bearer Token.

Example:

```http
Authorization: Bearer <access_token>
```

---

# Common HTTP Methods

| Method | Description |
|---------|-------------|
| GET | Retrieve data |
| POST | Create resources |
| PUT | Update resources |
| DELETE | Remove resources |

---

# Create a Project

### Endpoint

```http
POST /projects
```

### Request

```json
{
  "projectName": "Validation_Project_01",
  "owner": "Engineer01",
  "technology": "5nm"
}
```

### Response

```json
{
  "projectId": "P10045",
  "status": "Created"
}
```

---

# Get Project Details

### Endpoint

```http
GET /projects/{projectId}
```

### Sample Response

```json
{
  "projectId": "P10045",
  "projectName": "Validation_Project_01",
  "status": "Completed"
}
```

---

# Execute Validation

### Endpoint

```http
POST /validations
```

### Request

```json
{
  "projectId": "P10045",
  "validationProfile": "Regression"
}
```

### Response

```json
{
  "jobId": "JOB2345",
  "status": "Running"
}
```

---

# HTTP Status Codes

| Code | Description |
|------|-------------|
| 200 | Success |
| 201 | Resource Created |
| 400 | Bad Request |
| 401 | Unauthorized |
| 404 | Resource Not Found |
| 500 | Internal Server Error |

---

# Error Response

```json
{
  "errorCode": "API-401",
  "message": "Authentication Failed"
}
```

---

# Best Practices

- Use HTTPS.
- Authenticate every request.
- Validate request payloads.
- Handle HTTP status codes appropriately.
- Use pagination for large datasets.

---

# Related Documentation

- User Guide
- Administrator Guide
- CLI Reference
