# Skynet Logger 

**The Extraterrestrial Overlord of Logging Frameworks**

Welcome to **Skynet Logger**, the custom logger that beams down from the cosmos to bring structured and configurable logging to your codebase. Forget the days of primitive, unstructured logs—Skynet Logger is here to abduct your logging problems and replace them with beautifully formatted, context-rich logs that are light-years ahead.

---

## 🛸 Features
- **Dynamic Configuration**: Adjust log levels, formats, and destinations faster than a UFO entering hyperspace.  
- **Dual Output**: Logs to both console and file because why settle for one planet when you can conquer the galaxy?  
- **Contextual Logging**: Automatically includes the function name and optional context because context is universal.  
- **Error Handling**: Gracefully handles file logging issues without causing an interstellar catastrophe.  
- **Customizable Formats**: Choose your log format and date format like you're programming an alien mothership.

---

## 🛠️ Installation
Clone the repo and drop `CustomLogger.py` into your project like an alien artifact discovered in Area 51:  
```bash
git clone https://github.com/yourusername/SkynetLogger.git
```

---

## 👽 Usage
Here’s how to summon the extraterrestrial power of Skynet Logger:

```python
from CustomLogger import CustomLogger

# Configuration for the logger
config = {
    "enabled": True,
    "level": "DEBUG",
    "log_to_file": True,
    "log_file_path": "./skynet_logger.log",
    "log_to_console": True,
    "format": "%(asctime)s - %(name)s - %(levelname)s - %(message)s",
    "date_format": "%Y-%m-%d %H:%M:%S"
}

# Initialize the logger
logger = CustomLogger(config, logger_name="alien_app")

# Log messages with cosmic style
logger.debug("Debugging the alien tech", action="reverse engineering", success=True)
logger.info("Skynet Logger has landed!")
logger.warning("Warning: Unidentified log format detected!", location="Sector 7G")
logger.error("Error: Wormhole instability detected!", severity="high")
logger.critical("Critical: Black hole imminent!", evacuation="underway")
```

---

## 🧩 Configuration Options
| Option            | Description                                                                 | Default Value               |
|--------------------|-----------------------------------------------------------------------------|-----------------------------|
| `enabled`         | Enable or disable logging.                                                 | `True`                      |
| `level`           | Set the logging level (`DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL`).   | `INFO`                      |
| `log_to_file`     | Enable or disable logging to a file.                                       | `True`                      |
| `log_file_path`   | Path to the log file.                                                      | `./token_manager.log`       |
| `log_to_console`  | Enable or disable logging to the console.                                  | `True`                      |
| `format`          | Log message format.                                                       | `'%(asctime)s - %(name)s - %(levelname)s - %(message)s'` |
| `date_format`     | Date format for log timestamps.                                            | `'%Y-%m-%d %H:%M:%S'`       |

---

## 🛸 Why Skynet Logger?
Because your logs deserve to be more than just boring text files. With Skynet Logger, you get:  
- Logs that are **structured** and **readable**.  
- Contextual information that makes debugging feel like deciphering alien hieroglyphs.  
- A logger that’s as adaptable as an extraterrestrial shapeshifter.  

---

## 🌌 Contributing
Want to add more alien-themed features? Open a PR and let’s make Skynet Logger even more otherworldly!  

---

## 📜 License
This project is licensed under the MIT License. Because even aliens believe in open source.

---

## 👽 Fun Fact
Did you know? The Wow! signal detected in 1977 was a strong narrowband radio signal from space. That’s almost as powerful as Skynet Logger’s ability to decode your logging woes.
