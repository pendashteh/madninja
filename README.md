# madninja

Converts Markdown Ninja templates into **beautiful** websites you can host staticly!
## Project Overview

The goal of this project is to develop a Python script that automates the process of converting a folder of Markdown files to HTML and processing them as Ninja templates. The script should also be able to serve the processed files in a browser for testing purposes.

## Key Features

1. Convert Markdown files to HTML files.
2. Process HTML files as Ninja templates, excluding files with a `.tpl.html` extension.
3. Copy the `assets` folder from the source folder to the output folder.
4. Serve the output folder in a browser for testing purposes.
5. Allow user to define input and output folder names and locations.
6. Provide a command-line interface to build or serve the project.

## Deliverables

1. `markdown_ninja.py`: A Python script that implements the features mentioned above.
2. `README.md`: A brief documentation file that explains how to use the script and its features.
3. Sample folders: A sample input folder (`public_md`) and the resulting output folder (`public_html`) to demonstrate the script's functionality.

## Usage

### Build

To build the project, run the following command:

```
python3 markdown_ninja.py build -t /path/to/target-dir -m public_md -o public_html
```

### Serve

To serve the output folder, run the following command:

```
python3 markdown_ninja.py serve -t /path/to/target-dir -o public_html -p 8000
```

The script will serve the `public_html` folder at `http://localhost:8000` by default. The port number can be changed using the `-p` option.

## Dependencies

1. Python 3.6 or later
2. Markdown: `pip install markdown`
3. Jinja2: `pip install Jinja2`

## Future Improvements

1. Improve error handling and add user-friendly messages for various exceptions.
2. Add support for additional template engines.
3. Implement a watch mode that rebuilds the project automatically when source files are modified.
4. Add support for custom build configurations through a configuration file.
