# Redis Configuration Guide

## Basic Configuration

### Required Settings

1. **Password Settings**
   ```yaml
   allow_empty_password: true
   password: ""
   ```
   - Set `allow_empty_password` to false if using a password
   - Set `password` to your desired password if not allowing empty passwords

2. **Log Level**
   ```yaml
   log_level: info
   ```
   - Available levels: trace, debug, info, notice, warning, error, fatal
   - Default: info

3. **Extra Flags**
   ```yaml
   extra_flags: "--auto-aof-rewrite-percentage 100 --auto-aof-rewrite-min-size 64mb"
   ```
   - Configure Redis performance and persistence settings
   - Default settings optimize for Paperless-ngx usage

## Storage Configuration

Redis uses a single storage directory:

1. **Data Directory**
   - Location: `/data`
   - Contains: Redis database files and persistence data

## Port Configuration

- **Redis Port**: 6379
  - Access Redis at: `redis://[HOST]:6379`

## Backup Configuration

The following directories are excluded from backups:
- `**/data/**`

## Integration with Paperless-ngx

Redis is a required component for Paperless-ngx:

1. Paperless-ngx uses Redis for:
   - Caching
   - Message queuing
   - Task management
   - Session storage

2. Configuration Requirements:
   - Ensure Redis is accessible to Paperless-ngx
   - Configure appropriate password if needed
   - Set up persistence for data safety

## Security Considerations

1. Always set a strong password in production
2. Configure appropriate network access controls
3. Enable persistence for data safety
4. Regular backups recommended

## Performance Optimization

1. **Memory Management**
   - Configure appropriate memory limits
   - Monitor memory usage
   - Set up persistence for data safety

2. **Persistence Settings**
   - AOF (Append Only File) enabled by default
   - Automatic rewrite configured for optimal performance
   - Data durability ensured

3. **Connection Management**
   - Optimized for Paperless-ngx connections
   - Connection pooling enabled
   - Timeout settings configured
