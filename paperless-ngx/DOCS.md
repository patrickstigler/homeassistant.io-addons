# Paperless-ngx Configuration Guide

## Basic Configuration

### Required Settings

1. **Redis Connection**
   ```yaml
   redis_host: redis://[REDIS_HOST]:6379
   ```
   - Replace `[REDIS_HOST]` with the hostname or IP of your Redis server
   - Default port is 6379

2. **OCR Settings**
   ```yaml
   ocr_language: eng
   ```
   - Set the language for OCR processing
   - Common values: eng (English), deu (German), fra (French), etc.

3. **Time Zone**
   ```yaml
   time_zone: Europe/Berlin
   ```
   - Set your local time zone
   - Format: Continent/City (e.g., America/New_York, Europe/London)

### Optional Settings

1. **Log Level**
   ```yaml
   log_level: info
   ```
   - Available levels: trace, debug, info, notice, warning, error, fatal
   - Default: info

2. **Tika Integration**
   ```yaml
   tika_enabled: false
   tika_endpoint: ""
   tika_gotenberg_endpoint: ""
   ```
   - Enable Tika for enhanced document processing
   - Set Tika server endpoint if enabled
   - Set Gotenberg endpoint if using document conversion

3. **OCR Mode**
   ```yaml
   ocr_mode: redo
   ```
   - Options: skip, force, redo
   - Default: redo

4. **Consumer Polling**
   ```yaml
   consumer_polling: 0
   ```
   - Set polling interval for document consumers
   - 0 for continuous polling

5. **Secret Key**
   ```yaml
   secret_key: ""
   ```
   - Set a custom secret key for security
   - Leave empty for automatic generation

## Storage Configuration

Paperless-ngx uses several storage directories:

1. **Data Directory**
   - Location: `/data`
   - Contains: Database and configuration files

2. **Media Directory**
   - Location: `/media`
   - Contains: Processed documents and thumbnails

3. **Consume Directory**
   - Location: `/consume`
   - Contains: Documents waiting to be processed

4. **Export Directory**
   - Location: `/export`
   - Contains: Exported documents

## Port Configuration

- **Web Interface**: Port 8000
  - Access the web interface at: `http://[HOST]:8000`

## Backup Configuration

The following directories are excluded from backups:
- `**/data/**`
- `**/media/**`
- `**/consume/**`

## Security Considerations

1. Always set a strong secret key
2. Use secure passwords for Redis
3. Configure appropriate file permissions
4. Enable HTTPS for remote access
