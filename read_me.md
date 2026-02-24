# swagger-api-example

[Live Demo](https://hcwxd.github.io/swagger-api-example/index.html)

## Installation

1. Clone the repository: `git clone https://github.com/HcwXd/swagger-api-example.git`
2. Navigate to directory: `cd swagger-api-example`
3. Open `index.html` in your browser

## Quick Start

- View `index.html` for rendered documentation
- Review `swagger.json` for basic Swagger syntax
- Use VS Code with Swagger Viewer plugin for live editing

## Swagger Document Structure

### 1. Metadata
- API version and title
- Host URL and base path
- Category tags

### 2. API Endpoints
- HTTP methods (GET, POST, etc.)
- Request parameters and body
- Response schemas

### 3. Reusable Components
- Shared definitions via `$ref`

## Basic Syntax

### Metadata
```json
{
  "swagger": "2.0",
  "info": { "version": "1.0.0", "title": "API Example" },
  "host": "localhost",
  "basePath": "/v1"
}
```

### Parameters
```json
"parameters": [{
  "in": "query",
  "name": "id",
  "required": true,
  "type": "string"
}]
```

### Responses
```json
"responses": {
  "200": {
    "description": "Success",
    "schema": { "$ref": "#/definitions/User" }
  }
}
```

### Definitions
```json
"definitions": {
  "User": {
    "properties": {
      "id": { "type": "integer" },
      "name": { "type": "string" }
    }
  }
}
```

## Resources

- [Swagger Editor](https://editor.swagger.io)
- [OpenAPI Tutorial](https://apihandyman.io/writing-openapi-swagger-specification-tutorial-part-2-the-basics/)
