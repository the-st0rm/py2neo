[![Build Status](https://travis-ci.org/nigelsmall/py2neo.svg?branch=release%2F2.0)](https://travis-ci.org/nigelsmall/py2neo)

Py2neo 2.0
==========

Py2neo is a client library and comprehensive toolkit for working with Neo4j from within Python
applications and from the command line. The core library has no external dependencies and has been
carefully designed to be easy and intuitive to use.


Requirements
------------

- Python 2.7 / 3.3 / 3.4
- Neo4j 1.8 / 1.9 / 2.0 / 2.1 / 2.2 (the latest point release of each version is recommended)


Installation
------------

To install, run the following::

    $ pip install py2neo

Additions:
------------
I have added merge function to class py2neo.cypher.CreateStatement so you can use it with the builder to completely build a graph. 
That was a solution to [my question on stackoverflow.com](https://stackoverflow.com/questions/30843003/py2neo-constructing-graph-using-cypher-builders)

You can call the new function as follows <br/>
builder.merge(Node, array of labels, properties, [raw_on_conditional_query])<br/>
The function will find the node that matches the given label and properties. If the node isn't found it will create it and it will execute the condition given e.g., on submit SET x=1 ON CREATE SET y=1<br/>
Note that the optional raw_on_conditional_query is raw cypher query so you should make sure that data are escaped in it correctly. 



For more information, read through the [full introduction](http://py2neo.org/2.0/intro.html).

To get in touch, contact me via [email](mailto:nigel@py2neo.org) or on
[Twitter](https://twitter.com/neonige).

For the previous stable release, check out the [release/1.6.4 branch](https://github.com/nigelsmall/py2neo/tree/release/1.6.4).
