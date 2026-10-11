# Modules

- **`src.server`**: Initializes the FastMCP application and Uvicorn runner (`main`).
- **`src.config`**: Defines application settings (`Settings`) via Pydantic.
- **`src.tools.projects` & `src.tools.documents`**: MCP tool definitions for project listing/file reading and document search/reading/publishing.
- **`src.services.projects`**: `ProjectService` for discovering and reading project files under `projects_root`.
- **`src.services.documents`**: `DocumentService` for handling Markdown document aggregation, search, and publishing workflow.
- **`src.integrations.github.git` & `github`**: Git repository management, commit handling, and GitHub pull request creation.
- **`src.utils.paths`**: Path validation and file resolution utilities.
- **`src.schemas.*`**: Pydantic models for projects, documents, and common data structures.
