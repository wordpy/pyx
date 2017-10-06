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
`$ git clone https://github.com/wordpy/pyx/`

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

Why convert from PHP to Python?
-------------------------------
If you ask this question, you probably shouldn't use `pyx.php`.
There is nothing wrong with PHP, except that it's not Python.
So it's not Pythonic!

If you often have to go between the Python world and the PHP world
(WordPress, Drupal, or other PHP framework), you can feel my pains for
not being able to use tons and tons of native Python libraries with ease,
such as [SQLAlchemy](http://www.sqlalchemy.org/), Machine Learning,
Deep Learning such as TensorFlow, etc.

PHP frameworks such as WordPress do offer xml-rpc, wp-api, wp-cli,
and other APIs to interface with Python and other languages.
However, preparing Python programs for such APIs and having PHP to
interface with the API on the other end is error prone, not robust,
hard to troubleshoot on both ends, and not scalable.
Hence, enterprises, web, or big-data applications cannot rely on those APIs
for high-speed and high-volume Web applications and large scale data sets.

So comes `pyx.php` to PHP-to-Python programmers' rescue!
It's time to release the beast!

`pyx.php` is Robust
-------------------
I have been developing, deploying, and polishing this package on and off
for the past 3 years. `pyx.php` has been:

* deployed to hundreds of web sites,
* been used very day, hour, minute, and second,
* committed hundreds of millions of rows in MariaDB/MySql,
* instantiated hundreds of billions of Php.array() objects, etc.

License
-------
Currently there are 4 versions of `pyx.php` with various number of
Php.array() that can be instantiated:

1. Freeware (FREE unregistered license): 1,000 array()
2. FREE registered license.    10,000 array()
3. PAID registered license.   100,000 array()
4. PAID registered license. 1,000,000 array()

Beyond the limit of number of array() that can be instantiated as listed
above, all versions are identical.
There is no time limit or other limits whatsoever.

Please register at <https://wordpy.com/new-acct/> to download the FREE
register version or the PAID versions.
See LICENSE.md

Future Plans
------------
Of course the future dream for this `pyx.php` module is to open source it
under GPL, after there is `sufficient` demand.  We all know that there
are lots of ways to monetize with an open source business model.

You might ask, why don't you just open source now, so to generate more demand?
This theory is generally true from most popular software, but `pyx.php` is
most definitely not going to be a popular one. Why?

There are lots of smarter programmers than me.  The fact that a robust
PHP-to-Python emulation module like `pyx.php` has not been created
probably has to do with the fact that there will very little demand in the
future. However, someone like me still need to maintain and upgrade `pyx.php`
for the next 10+ years, and there should be some financial incentives
for me or/and others to support your enterprise or big-data needs.

After all, how much is it to pay for a low level Python programmer to deal
with PHP and Python libraries and compiled C codes, performance tuning,
testing, troubleshooting, etc?

Will they have the interest or the time to support your mission critical needs?

Either way, we will do our best to support the freeware and registered
versions. Please let us know if you have any comments or suggestsions.

Enjoy using `pyx.php`!
