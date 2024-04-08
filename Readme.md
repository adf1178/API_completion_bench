This project is to generate benchmarks for completing thrid-party APIs

## Data structure

Original file is `java_spring_api.json`

The followings are important keys of each item:

- project_name: The project name and corresponding version
- code: The function that contains the API (with comment)
- left_context: The code before `code`
- right_context: The code after `code`
- test_function: Test cases, may be empty
- import_text[List]: The import library of the file
- comment: The comment of the function that uses the API


## Generate benchmarks

### Fill the config.yaml

TYPE: `how/when/select`

whether use comment `USE_COMMENT: False`

whether use file context `USE_FILE_CONTEXT: False`

if use file context, how many lines before `LINE_BEFORE: 10`

whether use import message `USE_IMPORT_MESSAGE: True`

whether fill in the middle (use right context) `FILL_IN_THE_MIDDLE: False`

The filename of the saved benchmark file`SAVE_FILE_NAME: how_to_use_function_import`


### Run generate_benchmark.py


```
python generate_benchmark.py
```