# Filter Garden - Azikon

This project is for generating Lua code that will be used by our GenGen2 to generate future filters.
### Usage
The project can be run from the command line using the Lua interpreter. It reads a JSON file, processes it, and outputs a formatted Lua script.
### Running the Script
You can run the script with default configuration paths (using the `src/config.lua` file) or provide custom paths via command-line arguments:
```bash
lua src/main.lua
```
Or with custom paths:
```bash
lua src/main.lua custom.json output.lua
```

### Project Structure Overview
```
/root-directory
  ├── /src
  │   ├── main.lua             # Main script for executing the conversion
  │   ├── config.lua           # Configuration file for paths and settings
  │   ├── /modules             # Modules for specific functionalities
  │   │   ├── JsonFieldExtractor.lua   # Module for extarcting JSON file
  │   │   ├── Formatter.lua            # Module for formatting Lua tables from JSON data
  |   ├── /lib
  │   |   ├── dkjson.lua               # JSON handling library
  |   ├── /utils
  │   |   ├── ArgumentParser.lua           # Parse arguments or using `/src/config.lua`
  │   |   ├── Constants.lua                # Storing constants
  │   |   ├── FileOperations.lua           # Utils for files (e.g, writing a file)
  │   |   ├── JsonParser.lua               # Module for JSON file reading and parsing
  │   |   ├── Utils.lua                    # Module for general util functionalities
  ├── /docs-implemtation      # Declaration of documentation files for project details
  ├── main.lua             # Main script for executing the conversion

```
This project have been tested with lua 5.4, for both windows10&11 and also ubuntu LTS.
