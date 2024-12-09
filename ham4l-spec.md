# HAM4L (Hyper Application Model for LLM) Specification

HAM4L is a JSON-based model designed to describe applications and their interactions for LLM-driven solutions. 
It follows a structured approach to define applications, pages, UI elements, and events.

## Top-Level Structure

The top-level object contains two key sections:

- `ham4l`: Contains metadata about the HAM4L version and the default locale.
- `apps`: An array of applications.

Example:
```json
{
  "ham4l": {
    "version": "0.1.0",
    "default-locale": "en"
  },
  "apps": [
    ...
  ]
}
```
