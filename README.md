# 🚀 tldr-pages: Your Instant Command-Line Reference

<p align="center"><img src="./images/banner.png" alt="tldr-pages Banner" width="700"></p>

## Short Description
`tldr-pages` is a community-driven, concise, and indispensable collection of simplified command-line man pages. Forget sifting through exhaustive documentation; `tldr-pages` cuts straight to the chase, providing practical examples for everyday CLI tools across a multitude of platforms and languages. It's the ultimate cheat sheet for developers, system administrators, and anyone who navigates the terminal.

## ✨ Key Features
*   **Blazing Fast Answers**: Get right to the most common use cases of any command with practical examples, saving you precious time.
*   **Massively Multi-Platform**: Access simplified pages for `Linux`, `macOS (OSX)`, `Windows`, `Android`, `FreeBSD`, `SunOS`, and even `Cisco-IOS` environments.
*   **Globally Accessible**: With extensive localization support (including Arabic, Bengali, German, Spanish, French, Hindi, Indonesian, Italian, Japanese, Korean, Dutch, Norwegian, Polish, Brazilian Portuguese, European Portuguese, Romanian, Russian, Swedish, Tamil, Thai, Turkish, Ukrainian, Uzbek, Simplified Chinese, and Traditional Chinese), `tldr-pages` speaks your language.
*   **Community-Powered**: Driven by contributions from thousands of developers worldwide, ensuring accuracy, relevance, and constant growth.
*   **Developer-Friendly Workflow**: Features robust CI/CD pipelines, linting, and development container configurations to streamline contributions and maintain high-quality standards.
*   **Portable Documentation**: Easily generate platform-specific PDF documentation from the source files for offline reference or custom distribution.

## Who is this for?
`tldr-pages` is an essential resource for:
*   **Software Developers**: Quickly recall command syntax for git, Docker, Node.js, Python, and more.
*   **System Administrators**: Troubleshoot and manage systems efficiently with instant access to common network, disk, and process commands.
*   **DevOps Engineers**: Accelerate your daily tasks with quick references for Kubernetes (`kubectl`), cloud CLIs (`aws`, `az`, `gcloud`), and automation tools.
*   **CLI Enthusiasts**: Discover new flags and patterns, or simply refresh your memory on less-frequently used commands.
*   **Learners**: A gentle introduction to complex command-line tools, showing practical usage before deep diving into full man pages.

## Technology Stack & Architecture
At its core, `tldr-pages` leverages:
*   **Content**: Markdown (`.md`) for easily readable and maintainable command examples.
*   **Build & Automation**: Python (`scripts/*.py`), Shell scripting (`scripts/*.sh`), and Node.js (`package.json`, `package-lock.json`, `scripts/build-index.js`) for content processing, validation, and generation.
*   **Continuous Integration**: GitHub Actions (`.github/workflows`) orchestrates automated checks, content validation, and deployment.
*   **Developer Experience**: Visual Studio Code DevContainers (`.devcontainer`) provide a consistent and isolated development environment.
*   **Quality Assurance**: Tools like `flake8`, `codespell`, and `markdownlint` ensure code and content quality.
*   **Documentation Generation**: Custom Python scripts and CSS (`scripts/pdf/`) facilitate the creation of high-quality PDF outputs.

## 📊 Architecture & Database Schema
This project is primarily a content repository; its "architecture" focuses on content organization, contribution flow, and generation processes rather than a traditional database schema.

```mermaid
graph TD
    A[Community Contributor] --> B(GitHub Issues/PRs);
    B --> C{CI/CD Pipeline};
    C --> D[Markdown Content (pages/)];
    D -- "Processed by" --> E[Python/Shell Scripts (scripts/)];
    E -- "Generates" --> F[Rendered Output (e.g., PDF)];
    D -- "Accessed by" --> G[tldr-client CLI Applications];
```

## ⚡ Quick Start Guide
To get started with `tldr-pages` and explore its rich content:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/tldr-pages/tldr.git
    cd tldr
    ```

2.  **Explore the pages:**
    Browse the `pages/` directory to discover commands organized by language and platform.
    ```bash
    ls pages/common/ | head -n 5
    # Output:
    # %.md
    # $.md
    # !.md
    # ,.md
    # ...
    ```

3.  **Install Dependencies (for development/PDF generation):**
    ```bash
    npm install
    pip install -r scripts/pdf/requirements.txt
    ```

4.  **Generate PDF Documentation:**
    ```bash
    scripts/pdf/build-pdf.sh
    # You'll find the generated PDF in the 'docs' directory.
    ```

5.  **Contribute!**
    We welcome contributions! Please refer to [`CONTRIBUTING.md`](./CONTRIBUTING.md) for detailed guidelines.

## 📜 License
This project is licensed under the terms of the [MIT License](./LICENSE.md).