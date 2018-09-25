## Example:

```
Traceback (most recent call last):
  File "foobar.py", line 792, in <module>
    print value
UnicodeEncodeError: 'ascii' codec can't encode character u'\xa0' in position 20: ordinal not in range(128)
```

## From python

```python
import sys
import codecs
sys.stdout = codecs.getwriter('utf8')(sys.stdout)
sys.stderr = codecs.getwriter('utf8')(sys.stderr)
```

## When invoking a command

```bash
export PYTHONIOENCODING=UTF-8
```

or

```bash
PYTHONIOENCODING=UTF-8 ./manage.py runserver
```

source: https://chase-seibert.github.io/blog/2014/01/12/python-unicode-console-output.html
