Crawler Python API
____________________

Getting started with Crawler is easy.
The main class you need to care about is crawler.main.Crawler

.. autodoc:: crawler.main

crawler.utils

crawler.utils.should_ignore

.. testsetup::
	
	from crawler.utils import should_ignore

.. doctest::

	>>> should_ignore(['blog/$'], 'http://ericholscher.com/blog/')
	True

.. doctest::

	>>> should_ignore(['home'], 'http://ericholscher.com/blog/')
	True

.. testsetup::
	
	from crawler.utils import log

.. doctest::
	

	>>> log('http://ericholscher.com/blog/', 200)
	OK: 200 http://ericholscher.com/blog/ 

.. doctest::

	>>> log('http://ericholscher.com/blog/', 500)
	ERR: 500 http://ericholscher.com/blog/

.. doctest::

	>>> log('http://ericholscher.com/blog/', 500)
	OK: 500 http://ericholscher.com/blog/