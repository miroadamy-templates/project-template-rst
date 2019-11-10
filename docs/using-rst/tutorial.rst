
Notes from first steps
######################

Docker start
============

.. code:: bash

    mkdir first-rst
    docker run -it -v `pwd`/first-rst:/doc -e USER_ID=$UID ddidier/sphinx-doc:2.2.1-1 sphinx-init
    [sphinx-init] Generating documentation skeleton
    Welcome to the Sphinx 2.2.1 quickstart utility.

    Please enter values for the following settings (just press Enter to
    accept a default value, if one is given in brackets).

    Selected root path: .

    You have two options for placing the build directory for Sphinx output.
    Either, you use a directory "_build" within the root path, or you separate
    "source" and "build" directories within the root path.
    > Separate source and build directories (y/n) [n]:

    The project name will occur in several places in the built documentation.
    > Project name: first-notes
    > Author name(s): Miro Adamy
    > Project release []:

    If the documents are to be written in a language other than English,
    you can select a language here by its language code. Sphinx will then
    translate text that it generates into that language.

    For a list of supported codes, see
    https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-language.
    > Project language [en]:

    Creating file ./conf.py.
    Creating file ./index.rst.
    Creating file ./Makefile.

    Finished: An initial directory structure has been created.

    You should now populate your master file ./index.rst and create other documentation
    source files. Use the Makefile to build the docs, like so:
    make builder
    where "builder" is one of the supported builders, e.g. html, latex or linkcheck.

    [sphinx-init] Customizing Makefile
    [sphinx-init]   - Copying '/doc/Makefile' to '/doc/Makefile.bak'
    [sphinx-init]   - Adding 'livehtml' target to Makefile
    [sphinx-init] Customizing configuration
    [sphinx-init]   - Copying '/doc/conf.py' to '/doc/conf.py.bak'
    [sphinx-init]   - Adding extensions
    [sphinx-init]   - Enabling Markdown
    [sphinx-init]   - Enabling TODOs
    [sphinx-init] Adding resources
    [sphinx-init]   - Adding 'sphinxcontrib-excel-table' resources
    [sphinx-init] Adding pseudo extensions
    [sphinx-init] Adding utility scripts

    cd first-rst
    ll
    total 48
    -rw-r--r--  1 miro  staff   778B 31 Oct 17:45 Makefile
    -rw-r--r--  1 miro  staff   634B 31 Oct 17:45 Makefile.bak
    drwxr-xr-x  2 miro  staff    64B 31 Oct 17:45 _build
    drwxr-xr-x  3 miro  staff    96B 31 Oct 17:45 _python
    drwxr-xr-x  4 miro  staff   128B 31 Oct 17:45 _static
    drwxr-xr-x  3 miro  staff    96B 31 Oct 17:45 _templates
    drwxr-xr-x  7 miro  staff   224B 31 Oct 17:45 bin
    -rw-r--r--@ 1 miro  staff   4.1K 31 Oct 17:45 conf.py
    -rw-r--r--  1 miro  staff   1.8K 31 Oct 17:45 conf.py.bak
    -rw-r--r--  1 miro  staff   449B 31 Oct 17:45 index.rst
    cd ..

Docker cheatsheet
-----------------

.. code:: bash

    docker run --rm -it -v `pwd`/first-rst:/doc -e USER_ID=$UID ddidier/sphinx-doc:2.2.1-1 bash
    docker run --rm -it -v `pwd`/first-rst:/doc -e USER_ID=$UID ddidier/sphinx-doc:2.2.1-1 make html
    python -m http.server --directory first-rst/_build/html


    ddidier@4ea2ca65297d:/doc$ make help
    Sphinx v2.2.1
    Please use `make target' where target is one of
    html        to make standalone HTML files
    dirhtml     to make HTML files named index.html in directories
    singlehtml  to make a single large HTML file
    pickle      to make pickle files
    json        to make JSON files
    htmlhelp    to make HTML files and an HTML help project
    qthelp      to make HTML files and a qthelp project
    devhelp     to make HTML files and a Devhelp project
    epub        to make an epub
    latex       to make LaTeX files, you can set PAPER=a4 or PAPER=letter
    latexpdf    to make LaTeX and PDF files (default pdflatex)
    latexpdfja  to make LaTeX files and run them through platex/dvipdfmx
    text        to make text files
    man         to make manual pages
    texinfo     to make Texinfo files
    info        to make Texinfo files and run them through makeinfo
    gettext     to make PO message catalogs
    changes     to make an overview of all changed/added/deprecated items
    xml         to make Docutils-native XML files
    pseudoxml   to make pseudoxml-XML files for display purposes
    linkcheck   to check all external links for integrity
    doctest     to run all doctests embedded in the documentation (if enabled)
    coverage    to run coverage check of the documentation (if enabled)


Links on RestructuredText (Sphinx)
-----------------------------------
- https://www.sphinx-doc.org/en/master/
- https://www.sphinx-doc.org/es/master/usage/restructuredtext/index.html
- hosting on https://readthedocs.org/
- https://digitalsuperpowers.com/blog/2019-02-16-publishing-ebook.html
- https://restructuredtext.readthedocs.io/en/latest/
- https://pedrokroger.net/using-sphinx-write-technical-books/
