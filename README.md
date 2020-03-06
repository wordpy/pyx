Run Converted PHP Codes in Python at the Speed of Compiled-C
------------------------------------------------------------

`pyx.php` is a Cython compiled module that you can use to convert or
translate 99% of most common PHP source codes to pure Python.
In another words, it is a PHP-to-Python syntax emulation library in Cython.

The converted Python codes only require a Python 3.x interpreter,
the modules in the pyx repository, and some standard Python libraries.
PHP interpreter is not needed at all.

If we have already translated most of the WordPress core and other
scripts from PHP to Python using `pyx.php`, you can convert almost
any PHP code into Python.

With the speed of compiled Cython, running Python code translated from PHP
using `pyx.php` might be even faster than running the original PHP code in
the same computer.

Installation
------------
Download:

    $ git clone https://github.com/wordpy/wordpy/
    ls -la wordpy/pyx

Alternatively, you can:

    $ git clone https://github.com/wordpy/pyx/

You can download older version from your browser or from Linux shell:

    $ wget https://wordpy.com/pyx/pyx.tgz
    $ tar xvfpz pyx.tgz

Currently, `pyx.php` is only available for Python 3.x running 64-bit Linux.
Python 2.x, Mac, or other platforms can be compiled when there are many
requests.

Quick Start
-----------
`$ python # or ipython`

    >>> import pyx.php as Php; array = Php.array
    >>> arr1 = array( (0,'1-0'),('a','1-a'),('b','1-b'),)
    >>> arr2 = array( (0,'2-0'),(  1,'2-1'),('b','2-b'),('c','2-c'),)
    >>> arr1 + arr2   # same as: Php.array_plus(arr1, arr2), see below
    >>> Php.array_merge(arr1, arr2)
    
    >>> import pyx.php as Php;  array = Php.array
    >>> Arr0 = array()   # Arr0._obj is an empty OrderedDict()
    >>> Arr1 = array( ('a',11), 'zzz', (99,99), 22, 33, (2,22) )
    >>> Arr1
    array(6) {
      ['a']=> <int> 11
      [0]=> <str> zzz
      [99]=> <int> 99
      [100]=> <int> 22
      [101]=> <int> 33
      [2]=> <int> 22
    }

  `zip()` works for array with different len !!!

    >>> for i,j in zip( array(1,2,3,4), array(11,22,33) ):
    ...   print(i,j)
    1 11
    2 22
    3 33
    >>> for i,j in zip( array(1,2), array(11,22,33) ):
    ...   print(i,j)
    1 11
    2 22

Why convert from PHP to Python?
-------------------------------
If you ask this question, you probably shouldn't use `pyx.php`.
There is nothing wrong with PHP, except that it's not Python.
So it's not Pythonic!

If you often have to go between the Python world and the PHP world
(WordPress, Drupal, or other PHP framework), you can feel my pains for
not being able to use tons and tons of native Python libraries with ease,
such as SQLAlchemy, Machine Learning,
Deep Learning such as TensorFlow, etc.

PHP frameworks such as WordPress do offer xml-rpc, wp-api, wp-cli,
and other APIs to interface with Python and other languages.
However, preparing Python programs for such APIs and having PHP to
interface with the API on the other end is error prone, not robust,
hard to troubleshoot on both ends, and not scalable.
Hence, enterprises, web, or big-data applications cannot rely on those APIs
for high-speed and high-volume Web applications and large scale data sets.

Enjoy using `pyx.php`!
