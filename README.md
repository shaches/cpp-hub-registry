# cpp-hub Registry

This repository serves as the **official template registry** for the [cpp-hub](https://github.com/shaches/cpp-hub-demo) CLI tool. It hosts the master index of C++ project templates available for generation.

When you run `cpp-hub update` or `cpp-hub search`, the tool interacts with the `index.json` file in this repository to discover and retrieve template metadata.

## Available Templates

The registry currently contains the following templates:

| ID | Name | Description | Build System |
| :--- | :--- | :--- | :--- |
| `fmt-console-pm` | **fmt Console App (PM-selectable)** | Console app starter using `fmt`, with selectable package manager. | `cmake` |

## Registry Structure

The core of this repository is `index.json`, which defines the registry name and a map of available templates.

### Schema

Each entry in the `templates` object requires the following fields:

* **`id`**: A unique identifier for the template (e.g., `console-app-starter`).
* **`name`**: The human-readable name of the template.
* **`description`**: A brief summary of what the template provides.
* **`url`**: The Git clone URL for the template repository.
* **`tags`**: A list of strings to help users find the template via `cpp-hub search`.
* **`build_system`**: The primary build system used (e.g., `cmake`).

#### Example Entry

```json
"console-app-starter": {
  "id": "console-app-starter",
  "name": "Console App Starter",
  "description": "A small, modern CMake-based C++ console application with optional tests.",
  "url": "https://github.com/shaches/fmt-console-pm.git",
  "tags": ["console", "cmake", "starter"],
  "build_system": "cmake"
}
