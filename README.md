# Useful and Efficent Python Modules
List of useful python libraries and modules.

# Pathlib
This module offers classes representing filesystem paths with semantics appropriate for different operating systems.
Official website: <a href="https://docs.python.org/3/library/pathlib.html">link<a/> 
  
```python
from pathlib import Path
p = Path('.')
list_of_python_files = list(p.glob('**/*.py'))
```

# Smart Open
smart_open is a Python 2 & Python 3 library for efficient streaming of very large files from/to S3, HDFS, WebHDFS, HTTP, or local (compressed) files. It's a drop-in replacement for Python's built-in open(): it can do anything open can (100% compatible, falls back to native open wherever possible), plus lots of nifty extra stuff on top.
Official website: <a href="https://github.com/RaRe-Technologies/smart_open">link<a/>

`pip install smart_open`

```python
# stream lines from an S3 object
for line in smart_open('s3://mybucket/mykey.txt', 'rb'):
  print(line.decode('utf8'))

# stream from/to compressed files, with transparent (de)compression:
for line in smart_open('./foo.txt.gz', encoding='utf8'):
  print(line)
```
