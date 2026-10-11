# Architecture

DocMind MCP follows a modular layer architecture built around FastMCP:

- **Entry Point & Server (`src/server.py`):** Initializes the FastMCP server (`DocMind`), registers MCP tools, and exposes a stateless HTTP ASGI app via Uvicorn.
- **Configuration (`src/config.py`):** Loads environment variables using Pydantic `BaseSettings` for project paths, GitHub tokens, and repository settings.
- **Tools Layer (`src/tools/`):** Exposes FastMCP providers (`create_project_tools`, `create_document_tools`) wrapping underlying services.
- **Services Layer (`src/services/`):** Implements business logic for managing local project files (`ProjectService`) and documentation search, reading, and publishing (`DocumentService`).
- **Integrations (`src/integrations/github/`):** Handles Git operations and GitHub API interactions for publishing changes and PR creation.
