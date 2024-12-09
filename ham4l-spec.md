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

## Applications

Each application in the apps array contains:

- `id`: Unique identifier for the application.
- `name`: Localized name for the application.
- `description`: Localized description of the application.
- `pages`: An array of pages defining the structure of the application.
- `webapis`: An array of web apis defining the structure of the application.
- `logics`: An array of business logics defining the structure of the application.

Example:
```json
{
  "id": "example",
  "name": { "en": "Example App", "ja": "サンプルアプリ" },
  "description": { "en": "Example application of HAM4L.", "ja": "HAM4Lのサンプルアプリです。" },
  "pages": [
    ...
  ],
  "webapis": [
    ...
  ],
  "logics": [
    ...
  ]
}
```

## Pages

Each page contains:

- `id`: Unique identifier for the page.
- `name`: Localized name of the page.
- `type`: The type of page (e.g., signin, form).
- `layout`: An array of UI elements on the page.

## Layout Elements

The layout array defines the UI components on a page. Each element contains:

- `id`: Unique identifier for the element.
- `type`: The type of UI element (e.g., image, text_field, password_field, button).
- `label`: Localized label for input fields.
- `text`: Localized text for display or buttons.
- Additional properties depending on the element type (e.g., url for images, filters for input validation).

### Example UI Elements:

#### `text_field` Element:

#### `password_field` Element:

#### `image` Element:

### Events and Actions

Buttons can trigger events with a sequence of actions. Each action may have a condition determining if it executes.

## Localization Support

HAM4L supports multilingual applications through localized strings.

Example:
```json
{ "en": "Login", "ja": "ログイン" }
```
