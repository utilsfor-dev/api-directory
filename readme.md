# API Submission Guide

Thank you for your interest in contributing! To submit a new API to this directory, please follow the steps below.

## 1. Fork & Clone

- Fork this repository.
- Clone your fork to your local machine.

## 2. Add Your API

- Locate the API list file (e.g., `apis.json`).
- Add your API entry following this interface:

```typescript
interface API {
  id: string
  name: string
  isVerified?: boolean
  description: string
  category: string
  url: string
  pricing: "free" | "freemium" | "paid"
  documentation: string
  auth?: boolean
  https?: boolean
  cors?: boolean
  rateLimit?: string
}
```


### Allowed Categories

Please use one of the following categories for your API entry:

| `cat_id`       | Name          |
|----------------|---------------|
| `Development`    | Development   |
| `Weather`        | Weather       |
| `Payment`        | Payment       |
| `Geography`      | Geography     |
| `Images`         | Images        |
| `Email`          | Email         |
| `Finance`        | Finance       |
| `News`           | News          |
| `Communication`  | Communication |

> **Note:** 
> Use the `cat_id` value (e.g., `"Development"`, `"Weather"`) for the `category` field in your API entry.


- **Example:**

```json
[
  ...
  {
    "id": "example_api", // Use lowercase and underscores if the id contains spaces
    "name": "Example API",
    "description": "A sample API for demonstration purposes.",
    "category": "Weather",
    "url": "https://example.com/api",
    "pricing": "free",
    "documentation": "https://example.com/docs",
    "auth": true,
    "https": true,
    "cors": true,
    "rateLimit": "1,000 requests per day"
  }
]
```

## 3. Submit a Pull Request

- Commit your changes with a clear message.
  - Example: `Added [API name]`
- Push to your fork.
- Open a Pull Request (PR) to the `main` branch of this repository.

## 4. PR Review

- Your submission will be reviewed for completeness and accuracy.
- Please respond to any feedback or requested changes.

---

Thank you for contributing!

This project is sponsored by [JSONsilo.com](https://jsonsilo.com)