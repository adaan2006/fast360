[Read in Chinese (中文版)](https://github.com/shijincai/fast360/blob/main/README-zh.md)

# Fast360: A Tech-Focused OCR Model Arena 🚀

<p align="center">
  <img src="https://github.com/shijincai/fast360/blob/main/fast360-logo.png" alt="Fast360 Logo" width="150"/>
</p>

<p align="center">
  Fast360 is a free online platform aimed at solving a core technical pain point: quickly and intuitively evaluating and comparing the real-world performance of multiple open-source OCR engines on specific documents.
</p>

<p align="center">
  <a href="https://fast360.xyz" target="_blank">
    <img src="https://img.shields.io/badge/Try%20it%20Live-fast360.xyz-blue?style=for-the-badge&logo=rocket" alt="Try it Live">
  </a>
  <a href="#-tech-stack--implementation-details">
    <img src="https://img.shields.io/badge/Tech%20Stack-Node.js%20%7C%20Python%20%7C%20React-orange?style=for-the-badge" alt="Tech Stack">
  </a>
</p>

---

## 🤔 The Pain Point: Why Do We Need an "Arena"?

As developers and tech enthusiasts, we've all been through this process: for an OCR task, we find several seemingly powerful open-source models (like Marker, MinerU, PP-Structure, etc.). But what's next?

*   **Environment Hell:** Each model has its own unique `conda` environment, Python version, and CUDA dependencies. Switching between them for testing is time-consuming and exhausting.
*   **Lack of Real-World Standards:** Academic leaderboards are often based on standardized, clean datasets. They can't tell you which model will better handle the messy, scanned PDF with handwriting and tables you have on hand.
*   **Difficult Evaluation:** Manually comparing the Markdown outputs from different models, especially for long documents, is an extremely tedious and error-prone task.

We built Fast360 precisely to free developers from these repetitive and inefficient evaluation tasks.

## 🎯 Our Solution: A Dynamic, Hands-On Testing Platform

**Fast360 is not a static leaderboard, but a dynamic testing sandbox designed for real-world documents.** We handle all the backend model deployment, dependencies, and GPU scheduling, so you can focus on what matters most: **comparison and selection**.

## ✨ Core Features

*   **🧠 Multi-Model Parallel Processing:** Upload once and distribute the document to multiple independent OCR engines for parallel processing, significantly shortening the evaluation cycle.
*   **📝 Optimized for Markdown:** Focused on generating structured, code-friendly Markdown. We pay special attention to preserving heading levels, lists, tables, code blocks, and LaTeX formulas.
*   **🔬 Covers Diverse Scenarios:** From clean text optimized for RAG to preserving complex layouts in academic papers and digitizing handwritten notes, you can test all scenarios in one place.
*   **💸 Free & No Registration Required:** We believe good tools should be easy to use. The core comparison testing feature is completely free, available for immediate use without registration.

## 🛠️ The Arena's Model Lineup

We have curated a selection of open-source models that excel in specific domains. Understanding their characteristics will help you make better choices.

| Model | Core Strengths & Use Cases |
| :--- | :--- |
| **MinerU** | Academic papers, with good support for LaTeX formulas and multi-column layouts. |
| **MonkeyOCR** | Lightweight and fast, suitable for general-purpose scenarios with low layout requirements. |
| **Docling** | Advanced document understanding, aimed at producing "AI-Ready" text suitable for language models. |
| **Marker** | Specializes in extracting clean Markdown from PDFs, removing headers, footers, and other noise. |
| **Dolphin** | Adopts a "layout-first" strategy, analyzing page structure at high speed for excellent table and figure parsing. |
| **OCRFlux** | Its unique advantage is handling tables and paragraphs that span across multiple pages, ideal for long documents. |
| **PP-StructureV3** | A comprehensive document analysis engine from PaddleOCR, capable of outputting both Markdown and JSON. |
| *...we are continuously evaluating and integrating more great models!* | *Feel free to recommend new models you think are great in the [Issues](https://github.com/shijincai/fast360/issues).* |

## 🚀 Get Started in Seconds

No installation, no configuration. Just open your browser and begin your model evaluation journey.

### 👉 **[Try Fast360 Now for Free!](https://fast360.xyz)** 👈

Test with real data, make smarter choices.

---

## 🔧 Tech Stack & Implementation Details

We believe in technical transparency. The Fast360 platform is primarily composed of the following parts:

*   **Frontend:** Next.js 15 + React 19 + Ant Design, responsible for providing a smooth user experience and result presentation.
*   **Backend:** Node.js + Express + TypeScript, acting as a BFF layer to handle API requests, user management, and task scheduling.
*   **Task Queue:** Redis + BullMQ, responsible for asynchronously distributing OCR tasks to the GPU service with priority support.
*   **GPU Service:** Python + FastAPI, running on a dedicated GPU server. This service manages multiple Conda environments and invokes individual OCR model scripts via a command-line interface, handling the return of results.

## 🤝 Community & Contributions

This project was deeply inspired by tech communities like `r/LocalLLMA`. Although the platform itself is not an open-source project, we firmly believe its development should be community-driven.

We welcome all forms of feedback and contributions:

*   **Model Recommendations:** Have you discovered a new open-source model with stunning performance? Let us know in the [Issues](https://github.com/shijincai/fast360/issues)!
*   **Challenging Documents:** If you have a "model-killer" document, feel free to share it (after anonymization) to help us improve the platform's robustness.
*   **Feature Suggestions:** What other features do you think Fast360 should have? API support? More detailed performance metrics (processing time, CPU/GPU usage)?

We are building more than just a tool; we are building a community. Your voice is crucial.

---

<p align="center">
  <a href="https://fast360.xyz">Fast360.xyz</a> - The smarter PDF to Markdown tool, built for tech enthusiasts.
</p>
