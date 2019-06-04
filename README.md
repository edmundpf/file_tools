# Print Tools
[![Build Status](https://travis-ci.org/edmundpf/file_tools.svg?branch=master)](https://travis-ci.org/edmundpf/file_tools)
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
	* *get_file_lines*
		* returns list of lines from file
		* Args
			* *file* (string)
* **json_file**
	* *import_json*
		* returns dict object (or list) from file
		* Args
			* *file* (string)
	* *export_json*
		* exports dict object (or list) to file
		* Args
			* *data* (dict or list)
			* *file* (string)
			* *indent* (int) - number of spaces for json file indentation
