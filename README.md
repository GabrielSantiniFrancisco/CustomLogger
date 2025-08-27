# CustomLogger

A professional, flexible, and structured logging utility for Python applications. This module provides a configurable logger that supports both file and console output, dynamic log levels, and contextual message formatting. Designed for use in production-grade systems where detailed, readable, and easily managed logs are essential.

## Features

- **Configurable Logging**: Set log level, output format, date format, and enable/disable file or console logging via a configuration dictionary.
- **Dual Output**: Log messages to both file and console, or either, as needed.
- **Structured Context**: Each log message includes the module and function name, with optional contextual key-value pairs.
- **Dynamic Setup**: Easily integrate with any application by passing a config dict; no hardcoded paths or settings.
- **Error Handling**: Gracefully handles file handler setup errors, falling back to console logging if needed.
- **Simple API**: Standard logging methods (`debug`, `info`, `warning`, `error`, `critical`) with enhanced formatting.

## Usage

### 1. Installation
Copy `CustomLogger.py` into your project (e.g., in a `lib/` or `utils/` directory).

### 2. Example Configuration
```python
config = {
    'enabled': True,
    'level': 'INFO',
    'log_to_file': True,
    'log_file_path': './my_app.log',
    'log_to_console': True,
    'format': '%(asctime)s - %(name)s - %(levelname)s - %(message)s',
    'date_format': '%Y-%m-%d %H:%M:%S',
}
```

### 3. Basic Usage
```python
from CustomLogger import CustomLogger

logger = CustomLogger(config, logger_name="my_app")

logger.info("Application started")
logger.debug("Debugging details", user="alice", action="login")
logger.error("An error occurred", error_code=500)
```

### 4. Output Example
```
2025-08-27 12:00:00 - my_app - INFO - [Customlogger:main] - Application started
2025-08-27 12:00:01 - my_app - DEBUG - [Customlogger:some_function] - Debugging details | user=alice | action=login
2025-08-27 12:00:02 - my_app - ERROR - [Customlogger:some_function] - An error occurred | error_code=500
```

## API Reference

### `CustomLogger(config: dict, logger_name: str = "get_token")`
- **config**: Dictionary with logging options (see above).
- **logger_name**: Name for the logger instance (default: `get_token`).

#### Methods
- `debug(message: str, **kwargs)`
- `info(message: str, **kwargs)`
- `warning(message: str, **kwargs)`
- `error(message: str, **kwargs)`
- `critical(message: str, **kwargs)`

All methods accept a message and any number of keyword arguments for additional context.

## Advanced Details
- **Contextual Logging**: Each log entry includes the module and function name where the log was called, making it easy to trace issues.
- **No Duplicate Handlers**: Automatically clears existing handlers to prevent duplicate log entries.
- **Graceful Degradation**: If file logging fails (e.g., due to permissions), logs a warning and continues with console logging.

## License
MIT License

## Author
Gabriel Santini Francisco  
Email: gabrielsantinifrancisco@outlook.com

---

*For questions, suggestions, or contributions, please open an issue or pull request on the repository.*
