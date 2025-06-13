# IoT Setup & Support Guide

A DITA XML-based technical documentation project to guide users on setting up, configuring, and troubleshooting IoT devices. This project demonstrates practical application of DITA architecture, specialization, and multi-topic content organization, styled with custom CSS, and deployed via GitHub Pages.

## Introduction

This project was developed to serve as an example of using the **Darwin Information Typing Architecture (DITA)** for creating structured, modular, and reusable technical content for IoT device setup and support.

### Project Goals:

- Explain IoT basics, architecture, and usage.
- Provide task-based installation and configuration guides.
- Include reference matrices for devices and error codes.
- Feature specialized troubleshooting guides using custom DITA elements.
- Generate multi-page HTML5 output and deploy using GitHub Pages.

---

## DITA Structure Overview

The project includes **three main DITA topic types** plus a customized specialization:

### 1. Concept Topics

#### Purpose:
Introduce concepts clearly and simply, targeting beginners.

#### Key Elements Used:

| Element | Purpose |
|--------|---------|
| `<title>` | Provides the title of the concept. |
| `<shortdesc>` | Summarizes the topic in one sentence or paragraph for quick scanning. |
| `<conbody>` | Contains the main content of the concept. |
| `<section>` | Breaks the content into logical parts like definitions, benefits, and examples. |
| `<ul>`, `<li>` | Lists common IoT components. |
| `<image>`, `<alt>` | Adds visual aid (IoT ecosystem diagram). |
| `<xref>` | Cross-reference to the IoT architecture concept for continuity. |

---

### 2. Task Topics

#### Purpose:
Provide clear, step-by-step procedures for performing tasks like setup or configuration.

#### Key Elements Used:

| Element | Purpose |
|--------|---------|
| `<title>`, `<shortdesc>` | Task title and brief description. |
| `<taskbody>` | Contains structured task content. |
| `<prereq>` | Lists things required before starting (e.g., SSID/password). |
| `<context>` | Explains the task's importance or environment. |
| `<steps>`, `<step>` | Main step-by-step instructions. |
| `<cmd>` | Specific command or instruction text inside a step. |
| `<info>` | Extra information that may help during the task. |
| `<note>`, `<warning>` | Warnings (e.g., for firmware update risks) and important tips. |
| `<postreq>` | Instructions to follow after completing the task. |
| `<xref>` | Links to related tasks or troubleshooting guides. |

---

### 3. Reference Topics

#### Purpose:
Provide structured, easy-to-scan reference material (like matrices or error code tables).

#### Key Elements Used:

| Element | Purpose |
|--------|---------|
| `<refbody>` | Holds the entire reference content. |
| `<section>` | Logical sections within reference data. |
| `<table>` | Tabular data for devices, protocols, or error codes. |
| `<colspec>`, `<thead>`, `<tbody>`, `<row>`, `<entry>` | Build and format the table for clarity and consistency. |
| `<note>` | Provide tips, filtering notes for regions/products. |

---

### 4. Specialized Troubleshooting Topics

#### Purpose:
Offer structured problem-solving guidance using **custom DITA specialization** elements.

#### Files:
- `troubleshoot_connectivity.dita`
- `troubleshoot_app_integration.dita`
- `troubleshoot_firmware_issues.dita`

#### Key Specialized Elements Used:

| Element | Purpose |
|--------|---------|
| `<troubleshooting>` | Container for all troubleshooting content (custom element). |
| `<problem>` | Describes the issue (e.g., Wi-Fi not connecting). |
| `<cause>` | Lists possible reasons (e.g., wrong password). |
| `<remedy>` | Solutions with sub-steps (e.g., reboot router, switch bands). |
| `<ul>`, `<li>`, `<p>` | Structure remedies into readable sublists. |
| `<xref>` | Links to firmware updates or related tasks. |

---

### 5. DITA Map: `iot_guide.ditamap`

| Element | Purpose |
|--------|---------|
| `<map>` | Root element for organizing all topics. |
| `<topicref>` | References each DITA topic. |
| `<topichead>` | Groups topics into sections (Intro, Setup, Reference, Troubleshooting). |
| `@navtitle` | Sets navigation labels shown in output. |

---

## 🎨 CSS Styling Overview

- **Custom CSS file**: `/styles/my_style.css`
- Linked manually in all generated HTML files.

#### Manual Application:

| File | CSS Path |
|------|----------|
| `docs/index.html` | `styles/my_style.css` |
| `docs/outputs/topics/*.html` | `../../styles/my_style.css` |

#### Styles Included:

- Headings, paragraphs
- Table styling (borders, padding)
- Image scaling
- Lists
- Notes and warnings

---

## Output Generation & Deployment Process

1. **Generated Output**:  
   Used **DITA-OT (DITA Open Toolkit)** to convert XML to HTML5.

2. **Manual CSS Linking**:  
   Adjusted paths in generated HTML files to point to the correct `styles/my_style.css`.

3. **Preparing for GitHub Pages**:
   - Created `/docs` folder in project root.
   - Copied:
     - Final `index.html` (moved from `outputs` to `docs` root).
     - Entire `/outputs` folder (with topic HTML files).
     - `/styles` folder (with `my_style.css`).

4. **Pushed to GitHub**:
   - Committed and pushed all changes to the GitHub repository.

5. **GitHub Pages Configuration**:
   - Set GitHub Pages source to `/docs` folder.
   - Successfully deployed the site.

---

## Key Highlights

- ✅ Full DITA-based structured content creation.
- ✅ Use of **custom DITA specialization** for troubleshooting guides.
- ✅ Clean and consistent **manual CSS styling**.
- ✅ Manual handling of output paths for GitHub Pages compatibility.
- ✅ Successfully deployed as a live documentation website.

---

## View the Live Site

👉 [https://nenas97.github.io/IoT_Setup_Support/]

---

## Notes

- This project was developed as a **practice project to demonstrate DITA specialization, DITA-OT processing, and GitHub Pages deployment**.
- Manual control of file paths and CSS ensured full understanding of DITA output structure.
- All content has been AI-generated for this project.

