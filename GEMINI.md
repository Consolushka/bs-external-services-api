# BrainySoft External services - Bruno Workspace

## Project Overview
This directory serves as a **Bruno API client workspace** for managing external services related to BrainySoft. It provides a centralized location to organize and access various API collections, which are stored locally for easier sharing and version control.

- **Main Tool:** [Bruno](https://www.usebruno.com/) (Open-source IDE for API testing and development).
- **Structure:** The workspace is defined by `workspace.yml`, which manages links to API collections stored within the `collections/` directory.

## Key Files
- `workspace.yml`: The main configuration file for the Bruno workspace. It defines the workspace name and the paths to the included collections.
- `collections/`: Contains the API collections (e.g., Infotex). Each subdirectory here is a standalone Bruno collection.
- `.gitignore`: Standard git ignore file, configured to exclude secrets (`.env`), system files (`.DS_Store`), and dependencies (`node_modules`).

## Usage
To use this workspace:
1.  **Install Bruno:** Ensure you have the Bruno API client installed on your machine.
2.  **Open Workspace:** Launch Bruno and select **"Open Workspace"** and point it to this root directory.
3.  **Manage Collections:** All collections are located within the `collections/` directory. New collections should be added there and then linked in `workspace.yml`.
4.  **Environments:** Use Bruno's environment management to handle different base URLs or authentication secrets. Sensitive information should be kept in `.env` files (already git-ignored).

## Development Conventions
- **Collection Management:** When adding new collections, prefer placing them in the `collections/` directory or update `workspace.yml` to reflect external paths.
- **Secrets:** Never commit `.env` files or hardcode secrets within Bruno collection files. Use Bruno's environment variables.
- **Documentation:** Use the `docs` field in Bruno requests and collections to maintain up-to-date API documentation.
