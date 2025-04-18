[![Donate][donation-badge]](https://ko-fi.com/patrickstigler)

*Note: This donation badge is for the Home Assistant addon repository publication and not directly related to the Paperless-AI project.*

# Paperless-AI Addon for Home Assistant

This is the Home Assistant addon configuration for Paperless-AI, an intelligent document analyzer that enhances Paperless-ngx with AI capabilities.

## Features
- Automatic document analysis using OpenAI API or local models
- Smart tagging and categorization
- Document content understanding
- Integration with Paperless-ngx

![GitHub commit activity](https://img.shields.io/github/commit-activity/t/clusterzx/paperless-ai) ![Docker Pulls](https://img.shields.io/docker/pulls/clusterzx/paperless-ai) ![GitHub User's stars](https://img.shields.io/github/stars/clusterzx) ![GitHub License](https://img.shields.io/github/license/clusterzx/paperless-ai?cacheSeconds=1)
https://github.com/clusterzx/paperless-ai
# Paperless-AI

An automated document analyzer for Paperless-ngx using OpenAI API, Ollama and all OpenAI API compatible Services to automatically analyze and tag your documents. \
It features: Automode, Manual Mode, Ollama and OpenAI, a Chat function to query your documents with AI, a modern and intuitive Webinterface. \
\
**Following Services and OpenAI API compatible services have been successfully tested:**
- Ollama
- OpenAI
- DeepSeek.ai
- OpenRouter.ai
- Perplexity.ai
- Together.ai
- VLLM
- LiteLLM
- Fastchat
- Gemini (Google)
- ... and there are possibly many more

## Features

### Automated Document Management
- **Automatic Scanning**: Identifies and processes new documents within Paperless-ngx.
- **AI-Powered Analysis**: Leverages OpenAI API and Ollama (Mistral, Llama, Phi 3, Gemma 2) for precise document analysis.
- **Metadata Assignment**: Automatically assigns titles, tags, document_type and correspondent details.

### Advanced Customization Options
- **Predefined Processing Rules**: Specify which documents to process based on existing tags. *(Optional)* 🆕
- **Selective Tag Assignment**: Use only selected tags for processing. *(Disables the prompt dialog)* 🆕
- **Custom Tagging**: Assign a specific tag (of your choice) to AI-processed documents for easy identification. 🆕

### Manual Mode
- **AI-Assisted Analysis**: Manually analyze documents with AI support in a modern web interface. *(Accessible via the `/manual` endpoint)* 🆕

### Interactive Chat Functionality
- **Document Querying**: Ask questions about your documents and receive accurate, AI-generated answers. 🆕
