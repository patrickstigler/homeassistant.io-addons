# Paperless-AI Configuration Guide

## Basic Configuration

### Required Settings

1. **Paperless-ngx Connection**
   ```yaml
   paperless_url: http://[PAPERLESS_HOST]:[PAPERLESS_PORT]
   ```
   - Replace `[PAPERLESS_HOST]` with the hostname or IP of your Paperless-ngx server
   - Replace `[PAPERLESS_PORT]` with the port of your Paperless-ngx server (default: 8000)

2. **AI Model Configuration**
   ```yaml
   model: mistral
   ```
   - Available models: mistral, llama, phi3, gemma2
   - Default: mistral

### Optional Settings

1. **Log Level**
   ```yaml
   log_level: info
   ```
   - Available levels: trace, debug, info, notice, warning, error, fatal
   - Default: info

2. **OpenAI Integration**
   ```yaml
   openai_api_key: ""
   ```
   - Set your OpenAI API key if using OpenAI services
   - Leave empty if using local models only

3. **Ollama Integration**
   ```yaml
   ollama_url: http://[OLLAMA_HOST]:[OLLAMA_PORT]
   ```
   - Set Ollama server URL if using local models
   - Default port: 11434

## Storage Configuration

Paperless-AI uses a single storage directory:

1. **Data Directory**
   - Location: `/data`
   - Contains: Configuration and cache files

## Port Configuration

- **Web Interface**: Port 3233
  - Access the web interface at: `http://[HOST]:3233`

## Backup Configuration

The following directories are excluded from backups:
- `**/data/**`

## Security Considerations

1. Keep your OpenAI API key secure
2. Configure appropriate file permissions
3. Enable HTTPS for remote access
4. Use secure passwords for all services

## Integration with Paperless-ngx

Paperless-AI works best when properly integrated with Paperless-ngx:

1. Ensure Paperless-ngx is running and accessible
2. Configure the correct Paperless-ngx URL
3. Set up appropriate permissions for document access
4. Configure AI model settings based on your needs
