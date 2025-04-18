# Apache Tika Server Configuration Guide

## Basic Configuration

### Required Settings

1. **Log Level**
   ```yaml
   log_level: info
   ```
   - Available levels: trace, debug, info, notice, warning, error, fatal
   - Default: info

## Port Configuration

- **Server Port**: 9998
  - Access the Tika server at: `http://[HOST]:9998`

## Integration with Paperless-ngx

Apache Tika Server is optimized for use with Paperless-ngx:

1. No additional configuration needed
2. Paperless-ngx will automatically use Tika for metadata extraction
3. Ensure the correct port is accessible to Paperless-ngx

## Features

Apache Tika Server provides:

1. **Metadata Extraction**
   - Detects document types
   - Extracts metadata from various file formats
   - Supports over 1000 file types

2. **Content Analysis**
   - Extracts structured text content
   - Handles multiple languages
   - Supports various encodings

3. **Integration Capabilities**
   - REST API interface
   - Easy integration with other services
   - Optimized for document processing pipelines

## Security Considerations

1. Configure appropriate network access controls
2. No persistent storage required
3. Minimal attack surface
4. Regular updates recommended

## Performance Optimization

1. Runs in memory for optimal performance
2. Minimal resource requirements
3. Efficient document processing
4. Scalable architecture
