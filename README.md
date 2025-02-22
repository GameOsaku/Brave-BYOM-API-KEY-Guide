# Brave BYOM API Integration Guide

This guide provides instructions for integrating various AI models with Brave Browser's Bring Your Own Model (BYOM) feature. Brave Leo, the browser’s AI assistant, uses an OpenAI-compatible API implementation to connect to external models. This means your API endpoint must accept and process requests formatted according to the OpenAI API.

---

## Overview

Brave BYOM enables you to connect to external AI services by using endpoints and model identifiers that follow the OpenAI API specification. This guide covers three popular integrations:

- **GitHub Models** (via GitHub Inference API on Azure)
- **Google Gemini** (using the OpenAI Compatibility Layer)
- **DeepSeek AI**

---

## Supported Models

### 1. GitHub Models

- **Endpoint:**  
  `https://models.inference.ai.azure.com`  
  (Designed to accept OpenAI-style API requests.)

- **Model Name:**  
  Use the exact model identifier found in the "Code" section of your chosen GitHub Model page (e.g., `your-github-model-name`).

- **API Key:**  
  Obtain from the "Code" section of your GitHub Model page.

- **Reference Documentation:**  
  Check the [GitHub Models Prototyping Documentation](#) for details.

> **Note:** Ensure the selected GitHub Model supports API access.

---

### 2. Google Gemini

- **Endpoint:**  
  `https://generativelanguage.googleapis.com/v1beta/chat/completions`  
  *(Use this endpoint exclusively for Gemini integration.)*

- **Model Names:**  
  Examples include:
  - `gemini-1.5-flash-latest`
  - `gemini-1.5-pro-latest`
  - `gemini-pro-latest`  
  *Refer to the official Gemini API documentation for the latest model names.* [Models](https://ai.google.dev/gemini-api/docs/models/experimental-models) and [Experimental Models](https://ai.google.dev/gemini-api/docs/models/gemini) 

- **API Key:**  
  Obtain from [Google AI Studio](https://makersuite.google.com).

- **Reference Documentation:**  
  See the [Google AI Gemini API Quickstart](#) for guidance.

---

### 3. DeepSeek AI

- **Endpoint:**  
  `https://api.deepseek.com/chat/completions`

- **Model Names:**  
  Examples include:
  - `deepseek-chat`
  - `deepseek-reasoner`  
  *Consult the DeepSeek API documentation for the complete list.*

- **API Key:**  
  Obtain from your DeepSeek AI account dashboard.

- **Reference Documentation:**  
  Refer to the [DeepSeek AI API Documentation](#) for further instructions.

---

## Setup Instructions for Brave BYOM

In Brave Leo's BYOM configuration, enter the following details:

- **Label (Name):**  
  A descriptive name for your configuration (e.g., "GitHub Code Model", "Gemini Pro", "DeepSeek Chat").

- **Model Request Name (Model):**  
  The exact model identifier from your chosen provider.

- **Server Endpoint (Endpoint):**  
  Paste the appropriate OpenAI-compatible endpoint URL.

- **Context Window Size (Optional):**  
  Adjust if needed; the default is generally sufficient.

- **API Key:**  
  Enter the API key provided by your AI service.

---


## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve this guide.
