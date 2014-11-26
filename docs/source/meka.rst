Meka: python interface to java's meka library
=============================================


Setting up MEKA
---------------
In order to use the python interface to `MEKA <http://meka.sourceforge.net/>`_  you need to have JAVA and MEKA installed. Paths to both are passed to the class's constructor. To set up MEKA download the ``meka-<version>-realease.zip`` from `MEKA's sourceforge page <https://sourceforge.net/projects/meka/>`_, unzip it to ``<MEKA_DIR>`` and use ``<MEKA_DIR>/lib`` as the MEKA classpath for the constructor.

An example path to java might be: ``/usr/bin/java``, an example classpath to meka can be: ``/usr/local/meka-1.7/lib/``.

Using the interface
--------------------
To use the interface class start with importing skmultilearn's module, then create an object of the ``Meka`` class using the constructor, such as in the example:


.. code-block:
	import meka from meka
	meka = meka.Meka( 
		meka_classifier = "meka.classifiers.multilabel.LC", 
		weka_classifier = "weka.classifiers.bayes.NaiveBayes",
		meka_classpath = "/home/niedakh/pwr/old/meka-1.5/lib/", 
		java_command = '/usr/bin/java')

Where:

- ``meka_classifier`` is the MEKA classifier class selected from the MEKA API 
- ``weka_classifier`` is the WEKA classifier class selected from the WEKA API 