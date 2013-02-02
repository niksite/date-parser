date-parser
===========

Actually, this is just a wrapper around amazing dateutil library with a kind of i18n support.

You may use this as command line tool:

```
$ ./date_parser.py -h
Usage: date_parser.py [-f] [-q] <free-form date string>

Options:
  --version           show program's version number and exit
  -h, --help          show this help message and exit
  -f, --force-update  force self-updating of TRANSLATION_DICT in this file
  -q, --quiet         don't print debug messages to stdout
$ ./date_parser.py --version
0.2

$ python date_parser.py '13 августа 2010, 13:00'
DEBUG:date_parser:date_string has been translated to "13 August 2010, 13:00"
13 августа 2010, 13:00 -> 2010-08-13 13:00:00
```


Or as a usual library:

```
>>> from date_parser import parse
>>> print parse('17 April 2010 Saturday')
2010-04-17 00:00:00
>>> print type(parse('17 April 2010 Saturday'))
<type 'datetime.datetime'>
>>> print parse('воскресенье')
2010-04-18 00:00:00
```
