# github-demo
sample test with WSL
```


CakePHP Documentation
=====================

This is the official documentation for the CakePHP project. It is available online in HTML, PDF and EPUB formats at http://book.cakephp.org.

Requirements
------------

You can read all of the documentation within as its just in plain text files, marked up with ReST text formatting.  To build the documentation you'll need the following:

* Make
* Python
* Sphinx
* PhpDomain for sphinx

You can install sphinx using:

	easy_install sphinx

You can install the phpdomain using:

	easy_install sphinxcontrib-phpdomain

*To run the easy_install command, the setuptools package must be previously installed.*

Building the documentation
--------------------------

After installing the required packages, you can build the documentation using `Make`.

	# Create all the HTML docs. Including all the languages.
	make html
	
	# Create just the english HTML docs.
	make html-en
	
	# Create all the EPUB (e-book) docs.
	make epub
	
	# Create just the engish EPUB docs.
	make epub-en

	# Populate the search index
	make populate-index

This will generate all the documentation in an html form.  Other output such as 'pdf' and 'htmlhelp' are not fully complete at this time.

After making changes to the documentation, you can build the html version of the docs by using `make html` again.  This will build only the html files that have had changes made to them.


Contributing
------------

Contributing to the documentation is pretty simple. Please read the documentation on contributing to the documentation over on [the cookbook](http://book.cakephp.org/2.0/en/contributing/documentation.html) for help.

There are currently a number of outstanding issues that need to be addressed.  We've tried to flag these with `.. todo::` where possible.  To see all the outstanding todo's add the following to your `config/all.py`

	todo_include_todos = True

After rebuilding the html content, you should see a list of existing todo items at the bottom of the table of contents.

You are also welcome to make and suggestions for new content as commits in a github fork.  Please make any totally new sections in a separate branch.  This makes changes far easier to integrate later on.

Translations
------------

Contributing translations requires that you make a new directory using the two letter name for your language.  As content is translated, directories mirroring the english content should be created with localized content.


Generating Meta tags
--------------------

If you are providing translations and want to automatically generate meta tags for the resulting html files, a MetatagShell is provided in
the `scripts` folder of this repo. In order to use it, copy it into any CakePHP 2.0 empty application inside `app/Console/Command`, execute
`Console/cake metatag` and follow the instructions.

The script will process all the files under one of the translation folders and generate the possible description terms using an external API, 
it is a good idea to go over the generated terms and clean-up whatever noise it might have generated.

Making search work locally
--------------------------

* Install elasticsearch.  This varies based on your platform, but most
  package managers have a package for it.
* Clone the [docs_search](https://github.com/cakephp/docs_search) into a
  web accessible directory.
* Modify `searchUrl` in `themes/cakephp/static/app.js` to point at the
  baseurl for your docs_search clone.
* Start elasticsearch with the default configuration.
* Populate the search index using `make populate-index`.
* You should now be able to search the docs using elasticsearch.

