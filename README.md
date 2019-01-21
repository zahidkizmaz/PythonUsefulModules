# Useful and Efficent Python Modules
List of useful python libraries and modules.

# PyPy
PyPy is a fast, compliant alternative implementation of the Python language (2 and 3). It has several advantages and distinct features.

<p>Official website: <a href="http://pypy.org/">link<a/></p>
<p>DockerHub : <a href="https://hub.docker.com/_/pypy">link<a/></p>

# Pathlib
This module offers classes representing filesystem paths with semantics appropriate for different operating systems.
<p>Official website: <a href="https://docs.python.org/3/library/pathlib.html">link<a/> </p>
  
```python
from pathlib import Path
p = Path('.')
list_of_python_files = list(p.glob('**/*.py'))
```

# Smart Open
smart_open is a Python 2 & Python 3 library for efficient streaming of very large files from/to S3, HDFS, WebHDFS, HTTP, or local (compressed) files. It's a drop-in replacement for Python's built-in open(): it can do anything open can (100% compatible, falls back to native open wherever possible), plus lots of nifty extra stuff on top.
<p>Official website: <a href="https://github.com/RaRe-Technologies/smart_open">link<a/></p>

`pip install smart_open`

```python
# stream lines from an S3 object
for line in smart_open('s3://mybucket/mykey.txt', 'rb'):
  print(line.decode('utf8'))

# stream from/to compressed files, with transparent (de)compression:
for line in smart_open('./foo.txt.gz', encoding='utf8'):
  print(line)
```

# Bounter Counter
Bounter is a Python library, written in C, for extremely fast probabilistic counting of item frequencies in massive datasets, using only a small fixed memory footprint.
<p>Official website: <a href="https://github.com/RaRe-Technologies/bounter">link<a/></p>

`pip install bounter`

```python
from bounter import bounter

counts = bounter(size_mb=1024)  # use at most 1 GB of RAM
counts.update([u'a', 'few', u'words', u'a', u'few', u'times'])  # count item frequencies

print(counts[u'few'])  # query the counts
2
```
# SymPy
SymPy is a Python library for symbolic mathematics. It aims to become a full-featured computer algebra system (CAS) while keeping the code as simple as possible in order to be comprehensible and easily extensible.
<p>Official website: <a href="https://github.com/sympy/sympy">link<a/></p>

If you have conda:
`conda install sympy`
or
`pip install sympy`

```python
from sympy import Symbol, cos
x = Symbol('x')
e = 1/cos(x)
print e.series(x, 0, 10)
1 + x**2/2 + 5*x**4/24 + 61*x**6/720 + 277*x**8/8064 + O(x**10)
```
