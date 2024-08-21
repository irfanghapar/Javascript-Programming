<p align="center">
  <img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/ec559a9f6bfd399b82bb44393651661b08aaf7ba/icons/folder-markdown-open.svg" width="100" alt="project-logo">
</p>
<p align="center">
    <h1 align="center">README-AI</h1>
</p>
<p align="center">
    <em>Unleash AI magic on your documentation!</em>
</p>
<p align="center">
	<img src="https://img.shields.io/github/license/eli64s/readme-ai?style=default&logo=opensourceinitiative&logoColor=white&color=0080ff" alt="license">
	<img src="https://img.shields.io/github/last-commit/eli64s/readme-ai?style=default&logo=git&logoColor=white&color=0080ff" alt="last-commit">
	<img src="https://img.shields.io/github/languages/top/eli64s/readme-ai?style=default&color=0080ff" alt="repo-top-language">
	<img src="https://img.shields.io/github/languages/count/eli64s/readme-ai?style=default&color=0080ff" alt="repo-language-count">
<p>
<p align="center">
	<!-- default option, no dependency badges. -->
</p>

<br><!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary><br>

- [ Overview](#-overview)
- [ Features](#-features)
- [ Repository Structure](#-repository-structure)
- [ Modules](#-modules)
- [ Getting Started](#-getting-started)
  - [ Installation](#-installation)
  - [ Usage](#-usage)
  - [ Tests](#-tests)
- [ Project Roadmap](#-project-roadmap)
- [ Contributing](#-contributing)
- [ License](#-license)
- [ Acknowledgments](#-acknowledgments)
</details>
<hr>

##  Overview

The readme-ai project automates README file generation using AI models, enhancing documentation creation with dynamic badge generation, language model integration, and CLI interface. It parses various configuration and package files, generating insights crucial for repository analysis. The project streamlines Docker setup, PyPI deployment, code formatting, and testing processes, maximizing efficiency and security. With robust parsers for different languages and frameworks, readme-ai provides developers with a comprehensive toolkit for streamlined documentation and project management.

---

##  Features

|    |   Feature         | Description |
|----|-------------------|---------------------------------------------------------------|
| ⚙️  | **Architecture**  | The project has a well-structured architecture leveraging Python 3.10 and various libraries for AI and generative language tasks. It uses Google APIs for language generation, with clear separation of concerns and modular design. |
| 🔩 | **Code Quality**  | Codebase maintains high quality with adherence to Python best practices, PEP 8 conventions, and comprehensive unit tests. The use of tools like Pytest, Nox, and GitPython ensures robust code quality and consistency. |
| 📄 | **Documentation** | Extensive documentation includes setup instructions, API references, and code examples. README files, Makefile, and Dockerfile contain detailed explanations of setup and usage, aiding developers in understanding and contributing to the project effectively. |
| 🔌 | **Integrations**  | Integrates with Google APIs, GitPython for version control, and various libraries for AI tasks. Dependencies include Google Auth, OpenAI, Pydantic, and more. These integrations enhance the project's capabilities for language generation and model training. |
| 🧩 | **Modularity**    | The codebase exhibits high modularity with clear separation of concerns, reusable components, and well-defined interfaces. This modular design promotes code reusability, maintainability, and facilitates easy extension for new features or functionality. |
| 🧪 | **Testing**       | Testing is comprehensive with frameworks like Pytest and tools such as Nox for test automation and coverage reporting. The project follows test-driven development practices, ensuring code reliability and functionality across different Python versions. |
| ⚡️  | **Performance**   | The project demonstrates efficient performance with optimized resource usage for AI tasks and language generation. Leveraging powerful libraries and frameworks like TensorFlow and Google APIs, it achieves high-speed processing and effective utilization of computational resources. |
| 🛡️ | **Security**      | Security measures include handling user permissions, non-root user setup in Dockerfile, and secure package installations from PyPI. The project follows security best practices to protect data integrity, access control, and secure interactions with external services. |
| 📦 | **Dependencies**  | Key external dependencies include GitPython, toml, Google Auth, OpenAI, PyYAML, and more. These libraries enhance the project's functionality for AI tasks, language generation, and interaction with external services. |

---

##  Repository Structure

```sh
└── readme-ai/
    ├── .github
    │   ├── release-drafter.yml
    │   └── workflows
    ├── CHANGELOG.md
    ├── CODE_OF_CONDUCT.md
    ├── CONTRIBUTING.md
    ├── Dockerfile
    ├── LICENSE
    ├── Makefile
    ├── README.md
    ├── docs
    │   ├── css
    │   ├── docs
    │   ├── js
    │   └── overrides
    ├── examples
    │   ├── images
    │   └── markdown
    ├── mkdocs.yml
    ├── noxfile.py
    ├── poetry.lock
    ├── pyproject.toml
    ├── readmeai
    │   ├── __init__.py
    │   ├── _agent.py
    │   ├── _exceptions.py
    │   ├── cli
    │   ├── config
    │   ├── core
    │   ├── generators
    │   ├── models
    │   ├── parsers
    │   ├── services
    │   └── utils
    ├── scripts
    │   ├── clean.sh
    │   ├── docker.sh
    │   ├── pypi.sh
    │   └── run_batch.sh
    ├── setup
    │   ├── environment.yaml
    │   ├── requirements.txt
    │   └── setup.sh
    └── tests
        ├── __init__.py
        ├── cli
        ├── config
        ├── conftest.py
        ├── core
        ├── generators
        ├── models
        ├── parsers
        ├── services
        ├── test_agent.py
        ├── test_exceptions.py
        └── utils
```

---

##  Modules

<details closed><summary>.</summary>

| File                                                                             | Summary                                                                                                                                                                                                                                               |
| ---                                                                              | ---                                                                                                                                                                                                                                                   |
| [noxfile.py](https://github.com/eli64s/readme-ai/blob/master/noxfile.py)         | Ensures consistent Python package installation and runs comprehensive test suite across various Python versions. Maximizes test coverage and generates informative coverage reports for the readme-ai repository.                                     |
| [Dockerfile](https://github.com/eli64s/readme-ai/blob/master/Dockerfile)         | Implements a Docker setup with Python 3.10 for the readmeai package, ensuring isolated environment setup, non-root user handling, and CLI command execution. Enhances security by configuring user permissions and installing dependencies from PyPI. |
| [Makefile](https://github.com/eli64s/readme-ai/blob/master/Makefile)             | Manages code formatting, linting, cleaning, and testing processes.-Generates Conda package, requirements file, and searches specific words within the repository.-Executes git log and eliminates untracked files.                                    |
| [pyproject.toml](https://github.com/eli64s/readme-ai/blob/master/pyproject.toml) | Generates README files automatically using AI models. Key features include CLI interface, integration with large language models, and dynamic badge generation. Facilitates easy documentation creation for developers.                               |

</details>

<details closed><summary>scripts</summary>

| File                                                                                 | Summary                                                                                                                                                                                                                                                                                     |
| ---                                                                                  | ---                                                                                                                                                                                                                                                                                         |
| [pypi.sh](https://github.com/eli64s/readme-ai/blob/master/scripts/pypi.sh)           | Automates PyPI deployment for the readmeai package. Cleans, builds, and uploads distribution files using twine, updating the package on PyPI repository.                                                                                                                                    |
| [run_batch.sh](https://github.com/eli64s/readme-ai/blob/master/scripts/run_batch.sh) | Generates markdown files with dynamic content and badges for various GitHub repositories. Utilizes different styles and colors for badges, aligns content, and selects images to enhance visual appeal. Configures API options based on repository position in the array.                   |
| [clean.sh](https://github.com/eli64s/readme-ai/blob/master/scripts/clean.sh)         | Cleans build, test, coverage, and Python artifacts by removing various directories and file types. Provides commands to clean specific artifact types within the repository.                                                                                                                |
| [docker.sh](https://github.com/eli64s/readme-ai/blob/master/scripts/docker.sh)       | Builds, publishes, and deploys a Docker image for the main application. Utilizes Docker Buildx for multi-platform support. Key functions include image building, pushing, and buildx setup. Enhances deployment process efficiency and ensures availability across different architectures. |

</details>

<details closed><summary>setup</summary>

| File                                                                                       | Summary                                                                                                                                                                                                                                                               |
| ---                                                                                        | ---                                                                                                                                                                                                                                                                   |
| [environment.yaml](https://github.com/eli64s/readme-ai/blob/master/setup/environment.yaml) | Defines environment dependencies for the readmeai project, ensuring compatibility and reproducibility. Configures Python version, package manager, and dependencies from requirements.txt.                                                                            |
| [requirements.txt](https://github.com/eli64s/readme-ai/blob/master/setup/requirements.txt) | Lists Python package requirements and versions for the project, crucial for setting up dependencies and ensuring compatibility with specific Python versions.                                                                                                         |
| [setup.sh](https://github.com/eli64s/readme-ai/blob/master/setup/setup.sh)                 | Sets up the readmeai environment by ensuring dependencies and versions are met, creating the environment if needed, activating it, adjusting paths, and installing required packages. A comprehensive script for initializing the development environment seamlessly. |

</details>

<details closed><summary>readmeai</summary>

| File                                                                                      | Summary                                                                                                                                                                                                                                                             |
| ---                                                                                       | ---                                                                                                                                                                                                                                                                 |
| [_agent.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/_agent.py)           | Generates README.md file using AI for a repository. Orchestrates file generation process, handles API settings, clones repo, processes files, and builds markdown. Customizes image and content based on AI responses. Logs completion and shares generated README. |
| [_exceptions.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/_exceptions.py) | Encapsulates errors like CLI issues, failed repo cloning/validation, file system operations, file read/write failures, readme generation errors, and unsupported services.                                                                                          |

</details>

<details closed><summary>readmeai.parsers</summary>

| File                                                                                      | Summary                                                                                                                                                                                                                                                                             |
| ---                                                                                       | ---                                                                                                                                                                                                                                                                                 |
| [factory.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/factory.py) | Provides abstract factory for project file parsers, mapping file extensions to parser classes. Enhances repository architecture by organizing parser classes for various languages and frameworks. Facilitates flexible and extensible parsing functionalities within the codebase. |

</details>

<details closed><summary>readmeai.parsers.configuration</summary>

| File                                                                                                          | Summary                                                                                                                                                                                     |
| ---                                                                                                           | ---                                                                                                                                                                                         |
| [ansible.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/configuration/ansible.py)       | Parses Ansible configuration files** for the repository, enabling analysis of playbook.yml and ansible/site.yml files.                                                                      |
| [apache.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/configuration/apache.py)         | Extracts configuration settings from Apache httpd.conf files for the README.AI project.                                                                                                     |
| [docker.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/configuration/docker.py)         | Parses Docker configuration files for package names.-Extracts base images and versions from Dockerfiles.-Parses services from Docker Compose YAML files.-Handles parsing errors gracefully. |
| [nginx.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/configuration/nginx.py)           | Extracts configuration settings from Nginx files, vital for generating insights in the data parsing component of the parent repositorys architecture.                                       |
| [properties.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/configuration/properties.py) | Parses.properties configuration files to extract connection strings and package names, enhancing the repositorys parsing capabilities for diverse file formats.                             |

</details>

<details closed><summary>readmeai.parsers.orchestration</summary>

| File                                                                                                          | Summary                                                                                                                                |
| ---                                                                                                           | ---                                                                                                                                    |
| [kubernetes.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/orchestration/kubernetes.py) | Extracts Kubernetes configuration details from YAML files, vital for orchestrating deployments in the parent repositorys architecture. |

</details>

<details closed><summary>readmeai.parsers.package</summary>

| File                                                                                                | Summary                                                                                                                                                                                                                                                        |
| ---                                                                                                 | ---                                                                                                                                                                                                                                                            |
| [yarn.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/package/yarn.py)         | Parses package names from yarn.lock files using a regex pattern. Handles parsing errors gracefully.                                                                                                                                                            |
| [nuget.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/package/nuget.py)       | Parse NuGet.Config files for.NET configurations within the readme-ai repositorys structure.                                                                                                                                                                    |
| [maven.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/package/maven.py)       | Defines Maven dependency parsing for pom.xml files, extracting package names based on specified regex patterns. Handles parsing errors and considers dependencies containing spring. Implemented within the parsers module of the parent repository.           |
| [npm.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/package/npm.py)           | Parses dependencies from package.json and yarn.lock files for the parent repositorys architecture. Handles JSON decoding and regular expression parsing to extract package names efficiently.                                                                  |
| [gem.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/package/gem.py)           | Parses Gemfile.lock (Ruby) configuration files to extract key information.                                                                                                                                                                                     |
| [pip.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/package/pip.py)           | Extracts configuration data from Pip (requirements.txt, Pipfile) files, essential for managing dependencies and defining software packages. Serves as a key component in parsing and interpreting project setup requirements within the repositorys structure. |
| [composer.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/package/composer.py) | Parses PHP Composer configuration files, crucial in the codebase architecture for managing project dependencies effectively.                                                                                                                                   |
| [gradle.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/package/gradle.py)     | Parses Gradle dependency files in the package, extracting and formatting package names for build.gradle and build.gradle.kts.                                                                                                                                  |

</details>

<details closed><summary>readmeai.parsers.language</summary>

| File                                                                                             | Summary                                                                                                                                                                                                                                                                             |
| ---                                                                                              | ---                                                                                                                                                                                                                                                                                 |
| [cpp.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/language/cpp.py)       | Parses C/C++ project dependency files with extractors for CMakeLists.txt, configure.ac, and Makefile.am. Handles parsing errors and returns extracted dependencies, libs, and software. Key role in analyzing and extracting project dependencies for the repositorys architecture. |
| [go.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/language/go.py)         | Extracts dependency names from go.mod files using regex parsing, handling errors gracefully. Aids in retrieving package dependencies in the parent repositorys architecture.                                                                                                        |
| [swift.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/language/swift.py)   | Extracts Swift package names from Package.swift files by parsing URLs and dependencies, handling errors gracefully.                                                                                                                                                                 |
| [python.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/language/python.py) | Parses Python dependency files in the `readme-ai` repository. Extracts package names from `requirements.txt`, `pyproject.toml` (Poetry, Flit), `Pipfile`, `environment.yml`. Handles TOML and YAML formats, supporting various build systems such as Pipenv and Poetry.             |
| [rust.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/language/rust.py)     | Parses Rust cargo.toml files to extract package names. Handles parsing errors gracefully. Vital for parsing dependencies in Rust projects.                                                                                                                                          |

</details>

<details closed><summary>readmeai.parsers.infrastructure</summary>

| File                                                                                                                   | Summary                                                                                      |
| ---                                                                                                                    | ---                                                                                          |
| [terraform.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/infrastructure/terraform.py)           | Parses Terraform configuration files main.tf in the `readme-ai` repositorys parsers section. |
| [cloudformation.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/infrastructure/cloudformation.py) | Extract CloudFormation configurations from YAML files within the parent repository.          |

</details>

<details closed><summary>readmeai.parsers.cicd</summary>

| File                                                                                               | Summary                                                                                                                                                                                                                                     |
| ---                                                                                                | ---                                                                                                                                                                                                                                         |
| [bitbucket.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/cicd/bitbucket.py) | Parses Bitbucket Pipelines configuration files.                                                                                                                                                                                             |
| [jenkins.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/cicd/jenkins.py)     | Extracts configurations from Jenkinsfile for CI/CD pipeline setup.                                                                                                                                                                          |
| [travis.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/cicd/travis.py)       | Extracts configuration details from.travis.yml files for CI/CD workflows.                                                                                                                                                                   |
| [circleci.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/cicd/circleci.py)   | Extracts CircleCI configuration details using a dedicated parser within the projects parsers module.                                                                                                                                        |
| [gitlab.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/cicd/gitlab.py)       | Analyzes GitLab CI configuration files with a dedicated parser from the parsers module. This key functionality aligns with the project's architecture, enhancing the understanding and processing of CI/CD workflows within the repository. |
| [github.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/parsers/cicd/github.py)       | Extracts GitHub Actions configurations insights to streamline CI/CD workflows within the parent repository.                                                                                                                                 |

</details>

<details closed><summary>readmeai.config</summary>

| File                                                                                           | Summary                                                                                                                                                                                                                                                            |
| ---                                                                                            | ---                                                                                                                                                                                                                                                                |
| [validators.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/config/validators.py) | Validates Git settings, ensuring the correctness of repository URLs and names. Determines the Git service host, and extracts the repository name from provided URLs.                                                                                               |
| [settings.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/config/settings.py)     | Defines configuration settings for readme-ai package, including API, file paths, Git repository, Markdown templates, and text generation settings.-Loads base configuration and additional files for use in the CLI.-Validates and sanitizes input using Pydantic. |

</details>

<details closed><summary>readmeai.config.settings</summary>

| File                                                                                                      | Summary                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ---                                                                                                       | ---                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [parsers.toml](https://github.com/eli64s/readme-ai/blob/master/readmeai/config/settings/parsers.toml)     | Identifies project configuration files across various languages and frameworks for parsing and analysis.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [commands.toml](https://github.com/eli64s/readme-ai/blob/master/readmeai/config/settings/commands.toml)   | Defines language-specific commands for install, run, and test operations. Centralizes build and test processes across various programming languages for streamlined development efforts within the project ecosystem.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [blacklist.toml](https://github.com/eli64s/readme-ai/blob/master/readmeai/config/settings/blacklist.toml) | Defines excluded directories, file extensions, and names for preprocessing within the project. Maintains a blacklist to filter out unwanted items during processing and enhances the efficiency of the workflow by preventing unnecessary file operations.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [languages.toml](https://github.com/eli64s/readme-ai/blob/master/readmeai/config/settings/languages.toml) | Defines programming language extensions and their corresponding names for the project. Essential for mapping languages to their readable formats across the codebase. Helps optimize code analysis and documentation processes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [prompts.toml](https://github.com/eli64s/readme-ai/blob/master/readmeai/config/settings/prompts.toml)     | Define project characteristics via Markdown template; encapsulate architecture, code quality, documentation, integrations, modularity, testing, performance, security, dependencies, scalability in a table format. Show essential project details for analysis.**Logo DesignCreate engaging project logo with bold, readable letters on a white background, suitable for a tech-centered app. Consider project identity and style elements.**OverviewDescribe project purpose and features, emphasizing functionality and value proposition. Avoid deep technical details, focus on high-level overview, and mention the project name.**SloganCraft a compelling and concise slogan for project branding, engaging the audience without directly including the project name.**Mermaid DiagramVisualize project components and data/control flow through a Mermaid flowchart. Customize the flowchart to reflect project specifics and architecture. |
| [markdown.toml](https://github.com/eli64s/readme-ai/blob/master/readmeai/config/settings/markdown.toml)   | Defines Markdown template blocks for README.md, incorporating project logos, badges, and structured markdown elements like quick links and tables of contents.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [config.toml](https://github.com/eli64s/readme-ai/blob/master/readmeai/config/settings/config.toml)       | Defines default, GitHub, and OpenAI API settings as configuration for the README.AI project. Specifies Markdown templates, badges, and directory structure in the codebase for easy navigation and project overview.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

</details>

<details closed><summary>readmeai.generators</summary>

| File                                                                                               | Summary                                                                                                                                                                                                                                                                  |
| ---                                                                                                | ---                                                                                                                                                                                                                                                                      |
| [tree.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/generators/tree.py)             | Generates a visual representation of a directory tree structure for a code repository, enhancing repo organization and overview.                                                                                                                                         |
| [badges.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/generators/badges.py)         | Generates and formats SVG badges for README using shields.io and skill icons. Builds metadata and project dependency badges, organizing them into visually appealing HTML format for the README.                                                                         |
| [quickstart.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/generators/quickstart.py) | Generates the Quickstart section for the README, including setup commands and top language details based on code summaries, with error handling and logging.                                                                                                             |
| [utils.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/generators/utils.py)           | Defines functions to eliminate default emojis from markdown content, split Markdown headings into sections, and update heading names for a cleaner display. These utilities facilitate organizing and enhancing the readability of Markdown documents in the repository. |
| [builder.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/generators/builder.py)       | Header, code summaries, directory tree, Getting Started, Contributing. Removes emojis based on config. Integrates badges, tables, setup data, and Git info dynamically for repository structure coherence.                                                               |
| [tables.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/generators/tables.py)         | Generates markdown tables for LLM text responses in README file based on code summaries, project structure, and repository URL. Organizes data by sub-directories, constructs links, and formats tables with column widths.                                              |

</details>

<details closed><summary>readmeai.models</summary>

| File                                                                                     | Summary                                                                                                                                                                                                                                  |
| ---                                                                                      | ---                                                                                                                                                                                                                                      |
| [openai.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/models/openai.py)   | Implements OpenAI API LLM handling with Ollama support. Initializes settings, builds payload for requests, and processes responses. Includes retry logic for error handling. Maintains authentication headers and logging.               |
| [gemini.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/models/gemini.py)   | Implements Google Clouds Gemini API handler with error handling and text generation capabilities. Initializes API settings, builds payload for requests, and processes API responses for text generation.                                |
| [factory.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/models/factory.py) | Defines a ModelFactory that orchestrates the selection of appropriate LLM handlers based on CLI input, enhancing the repositorys architecture by enabling dynamic handler selection for different services.                              |
| [dalle.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/models/dalle.py)     | Generates and downloads images via OpenAIs DALL-E model. Initializes model settings, formats prompts for image generation, and handles errors. Retrieves image URL and downloads the image from the provided link.                       |
| [prompts.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/models/prompts.py) | Generates and formats prompts for the LLM API based on provided context. Retrieves and injects template content. Sets additional and summary contexts with dependencies and file summaries, enhancing API responses.                     |
| [tokens.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/models/tokens.py)   | Handles tokenization, truncation, and token count validation for prompts in a language model. Caches encodings for efficiency and adjusts max token limits based on specific prompts. Logs errors for encoding and truncation processes. |
| [offline.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/models/offline.py) | Handles offline operations in the CLI, replicating LLM API responses. Initializes default settings and constructs placeholder text when API not available, mirroring expected API behavior.                                              |

</details>

<details closed><summary>readmeai.services</summary>

| File                                                                                         | Summary                                                                                                                                                                                                                                                                               |
| ---                                                                                          | ---                                                                                                                                                                                                                                                                                   |
| [git.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/services/git.py)           | Clone, validate repos, find API and file URLs, locate git executable, and verify file permissions. Resolves handling various git services and system platforms.                                                                                                                       |
| [metadata.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/services/metadata.py) | Retrieve metadata of a Git repository from the host providers API. Parse and fetch detailed repository information including statistics, details, URLs, programming languages, topics, settings, and license data. Ideal for extracting comprehensive data about GitHub repositories. |

</details>

<details closed><summary>readmeai.utils</summary>

| File                                                                                                  | Summary                                                                                                                                                                                                                                               |
| ---                                                                                                   | ---                                                                                                                                                                                                                                                   |
| [file_resources.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/utils/file_resources.py) | Retrieves absolute path to package resource file, prioritizing `importlib.resources` and fallback to `pkg_resources`. Handles exceptions and raises `FileReadError` if resource file is inaccessible.                                                 |
| [text_cleaner.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/utils/text_cleaner.py)     | Cleans and formats text responses from the LLM API. Processes feature-type responses into markdown tables and tidies generated text. Fixes markdown table formatting for feature and description columns.                                             |
| [file_handler.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/utils/file_handler.py)     | Handles reading and writing various file types using specialized methods. Caches file content for efficiency, supporting formats like JSON, Markdown, TOML, TXT, and YAML. Centralizes file operations to ensure consistency and ease of maintenance. |

</details>

<details closed><summary>readmeai.core</summary>

| File                                                                                         | Summary                                                                                                                                                                                                                                                                                    |
| ---                                                                                          | ---                                                                                                                                                                                                                                                                                        |
| [preprocess.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/core/preprocess.py) | Generates FileContext instances, processes repository files, and extracts dependencies using the factory pattern. Returns context, dependencies, and raw files for further processing and metadata extraction in the repository architecture.                                              |
| [utils.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/core/utils.py)           | Defines utility methods to configure LLM API environments, setting it to offline mode if necessary. Determines environment variables for different LLM services based on user input or existing configurations, ensuring proper API key presence.                                          |
| [logger.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/core/logger.py)         | Implements a custom logger with emoji and color support for the readme-ai package. Registers different log levels with corresponding emojis and colors. Provides methods to log messages with different severity levels in the application.                                                |
| [models.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/core/models.py)         | Handles generating text responses from Large Language Model (LLM) API based on prompts and dependencies. Manages HTTP client lifecycle, processes batch requests, and generates summaries for project files. Implements abstract methods for custom API settings and request construction. |
| [parsers.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/core/parsers.py)       | Defines an abstract base class for parsing dependency files. It includes methods for parsing file content, logging errors, and handling parsing exceptions. This code plays a crucial role in the architecture for processing dependency information within the project.                   |

</details>

<details closed><summary>readmeai.cli</summary>

| File                                                                                  | Summary                                                                                                                                                                                                                                                            |
| ---                                                                                   | ---                                                                                                                                                                                                                                                                |
| [main.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/cli/main.py)       | Entrypoint command line interface for readme-ai package with options for customization. Executes readme_agent function with specified parameters. Facilitates seamless interaction with the readme-ai toolkit for generating README files based on various inputs. |
| [options.py](https://github.com/eli64s/readme-ai/blob/master/readmeai/cli/options.py) | Defines CLI options for badge styles, header images, and LLM service choices, facilitating dynamic README.md generation based on user input.                                                                                                                       |

</details>

<details closed><summary>.github</summary>

| File                                                                                               | Summary                                                                                                                                                                                                                                                                                                                  |
| ---                                                                                                | ---                                                                                                                                                                                                                                                                                                                      |
| [release-drafter.yml](https://github.com/eli64s/readme-ai/blob/master/.github/release-drafter.yml) | Generates release notes based on specified labels and templates in accordance with Keep a Changelog conventions. Categorizes changes into features, bug fixes, chores, deprecations, removals, security, documentation, and dependency updates. Resolves version based on labeled changes and formats changelog entries. |

</details>

<details closed><summary>.github.workflows</summary>

| File                                                                                                           | Summary                                                                                                                                                                                                                  |
| ---                                                                                                            | ---                                                                                                                                                                                                                      |
| [release-pipeline.yml](https://github.com/eli64s/readme-ai/blob/master/.github/workflows/release-pipeline.yml) | Automates release workflow. Triggers pipeline on new release events to build, test, and deploy the README AI project. Implements continuous integration and delivery for seamless software releases.                     |
| [coverage.yml](https://github.com/eli64s/readme-ai/blob/master/.github/workflows/coverage.yml)                 | Automatically generates code coverage reports for every pull request using GitHub Actions. Helps maintain code quality standards within the project architecture by providing visibility on test coverage effectiveness. |
| [release-drafter.yml](https://github.com/eli64s/readme-ai/blob/master/.github/workflows/release-drafter.yml)   | Automates release notes generation based on merged pull requests. Configures release-drafter GitHub action to draft release notes automatically. Enhances project transparency and communication with contributors.      |

</details>

---

##  Getting Started

**System Requirements:**

* **Python**: `version x.y.z`

###  Installation

<h4>From <code>source</code></h4>

> 1. Clone the readme-ai repository:
>
> ```console
> $ git clone https://github.com/eli64s/readme-ai
> ```
>
> 2. Change to the project directory:
> ```console
> $ cd readme-ai
> ```
>
> 3. Install the dependencies:
> ```console
> $ pip install -r requirements.txt
> ```

###  Usage

<h4>From <code>source</code></h4>

> Run readme-ai using the command below:
> ```console
> $ python main.py
> ```

###  Tests

> Run the test suite using the command below:
> ```console
> $ pytest
> ```

---

##  Project Roadmap

- [X] `► INSERT-TASK-1`
- [ ] `► INSERT-TASK-2`
- [ ] `► ...`

---

##  Contributing

Contributions are welcome! Here are several ways you can contribute:

- **[Report Issues](https://github.com/eli64s/readme-ai/issues)**: Submit bugs found or log feature requests for the `readme-ai` project.
- **[Submit Pull Requests](https://github.com/eli64s/readme-ai/blob/main/CONTRIBUTING.md)**: Review open PRs, and submit your own PRs.
- **[Join the Discussions](https://github.com/eli64s/readme-ai/discussions)**: Share your insights, provide feedback, or ask questions.

<details closed>
<summary>Contributing Guidelines</summary>

1. **Fork the Repository**: Start by forking the project repository to your github account.
2. **Clone Locally**: Clone the forked repository to your local machine using a git client.
   ```sh
   git clone https://github.com/eli64s/readme-ai
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to github**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.
8. **Review**: Once your PR is reviewed and approved, it will be merged into the main branch. Congratulations on your contribution!
</details>

<details closed>
<summary>Contributor Graph</summary>
<br>
<p align="center">
   <a href="https://github.com{/eli64s/readme-ai/}graphs/contributors">
      <img src="https://contrib.rocks/image?repo=eli64s/readme-ai">
   </a>
</p>
</details>

---

##  License

This project is protected under the [SELECT-A-LICENSE](https://choosealicense.com/licenses) License. For more details, refer to the [LICENSE](https://choosealicense.com/licenses/) file.

---

##  Acknowledgments

- List any resources, contributors, inspiration, etc. here.

[**Return**](#-overview)

---
