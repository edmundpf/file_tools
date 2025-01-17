# File Tools
[![Build Status](https://travis-ci.org/edmundpf/file_tools.svg?branch=master)](https://travis-ci.org/edmundpf/file_tools)
[![PyPI version](https://badge.fury.io/py/file-tools.svg)](https://badge.fury.io/py/file-tools)
> Includes useful methods for file/json file reading and writing.
## Install
* `python3 -m pip install file-tools`
## Usage
``` python
from file_tools.file import get_file_string, get_file_lines
from file_tools.json_file import import_json, export_json
my_text = get_file_string('text.txt')
my_lines = get_file_lines('text.txt')
my_dict = import_json('example.json')
my_dict['test'] = 1
export_json(data=my_dict, file='example.json')
```
## Methods
* **file**
	* *get_file_string*
		* returns string from file
		* Args
			* *file* (string)
			* *path* (string=''), if empty path will be relative of CWD, otherwise will be relative of path, useful with os.path.abspath(__file__) to get file relative to module
			* *encoding* (string='utf-8'), encoding type, defaults to utf-8
	* *get_file_lines*
		* returns list of lines from file
		* Args
			* *file* (string)
			* *path* (string=''), if empty path will be relative of CWD, otherwise will be relative of path, useful with os.path.abspath(__file__) to get file relative to module
			* *newline* (sting='\n'), newline character to parse
			* *encoding* (string='utf-8'), encoding type, defaults to utf-8
	* *write_file_string*
		* writes file string to file
		* Args
			* *file* (string)
			* *path* (string=''), if empty path will be relative of CWD, otherwise will be relative of path, useful with os.path.abspath(__file__) to get file relative to module
			* *text* (string=''), string to write
			* *encoding* (string='utf-8'), encoding type, defaults to utf-8
	* *append_file_string*
		* appends file string to file
		* Args
			* *file* (string)
			* *path* (string=''), if empty path will be relative of CWD, otherwise will be relative of path, useful with os.path.abspath(__file__) to get file relative to module
			* *text* (string=''), string to write
			* *encoding* (string='utf-8'), encoding type, defaults to utf-8
	* *write_file_lines*
		* appends file lines to file
		* Args
			* *file* (string)
			* *path* (string=''), if empty path will be relative of CWD, otherwise will be relative of path, useful with os.path.abspath(__file__) to get file relative to module
			* *lines* (list=[]), lines to write
			* *newline* (sting='\n'), newline character to separate lines
			* *encoding* (string='utf-8'), encoding type, defaults to utf-8
	* *append_file_lines*
		* appends file lines to file
		* Args
			* *file* (string)
			* *path* (string=''), if empty path will be relative of CWD, otherwise will be relative of path, useful with os.path.abspath(__file__) to get file relative to module
			* *lines* (list=[]), lines to write
			* *newline* (sting='\n'), newline character to separate lines
			* *encoding* (string='utf-8'), encoding type, defaults to utf-8
* **json_file**
	* *import_json*
		* returns dict object (or list) from file
		* Args
			* *file* (string)
			* *path* (string=''), if empty path will be relative of CWD, otherwise will be relative of path, useful with os.path.abspath(__file__) to get file relative to module
	* *export_json*
		* exports dict object (or list) to file
		* Args
			* *data* (dict or list)
			* *file* (string)
			* *indent* (int) - number of spaces for json file indentation
			* *path* (string=''), if empty path will be relative of CWD, otherwise will be relative of path, useful with os.path.abspath(__file__) to get file relative to module
