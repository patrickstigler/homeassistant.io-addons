# Gotenberg Configuration Guide

## Basic Configuration

### Required Settings

1. **Log Level**
   ```yaml
   log_level: info
   ```
   - Available levels: trace, debug, info, notice, warning, error, fatal
   - Default: info

2. **Chromium Settings**
   ```yaml
   disable_javascript: true
   allow_list: file:///tmp/.*
   ```
   - Disable JavaScript for security
   - Configure allowed file access patterns

## Port Configuration

- **API Port**: 3000
  - Access the API at: `http://[HOST]:3000`

## Command Line Arguments

Gotenberg is configured with the following command line arguments:
```yaml
args:
  - gotenberg
  - --chromium-disable-javascript=true
  - --chromium-allow-list=file:///tmp/.*
```

These settings are optimized for use with Paperless-ngx and ensure secure document processing.

## Integration with Paperless-ngx

Gotenberg works seamlessly with Paperless-ngx for document conversion:

1. No additional configuration needed
2. Paperless-ngx will automatically use Gotenberg for document conversion
3. Ensure the correct port is accessible to Paperless-ngx

## Security Considerations

1. JavaScript is disabled by default for security
2. File access is restricted to the /tmp directory
3. No persistent storage is required
4. Configure appropriate network access controls

## Performance Optimization

1. Gotenberg runs in memory for optimal performance
2. No persistent storage means faster document processing
3. Chromium settings are optimized for document conversion
4. Resource usage is minimal
