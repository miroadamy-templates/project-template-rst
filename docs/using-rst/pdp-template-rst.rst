.. sectionauthor:: Le Yang <le.yang@leidoshealth.com>

.. _pdp-template-rst:
.. _pdp:
.. _pdp-template-txt:

####################################
Sample reStructuredText PDP Template
####################################

:Service: All
:Function: Patient Care
:Type: Process
:Module: N/A
:Status: Final

Abstract
========

This PDP provides a boilerplate or sample template for creating your
own reStructuredText PEPs.  In conjunction with the content guidelines
in :ref:`pdp`, this should make it easy for you to conform your own
PEPs to the format outlined below.

Note: if you are reading this template via the web, you should first grab 
the text (reStructuredText) source of this PDP in order to complete
the steps below.  **DO NOT USE THE HTML FILE AS YOUR TEMPLATE!**

The source for this (or any) template can be :download:`downloaded here <pdp-template-rst.rst>`.

If you would prefer not to use markup in your PDP, please see :ref:`pdp-template-txt`.


Rationale
=========

PDP submissions come in a wide variety of forms, not all adhering
to the format guidelines set forth below.  Use this template, in
conjunction with the format guidelines below, to ensure that your
PDP submission won't get automatically rejected because of form.

ReStructuredText is offered as an alternative to plaintext PEPs, to
allow PDP authors more functionality and expressivity, while
maintaining easy readability in the source text.  The processed HTML
form makes the functionality accessible to readers: live hyperlinks,
styled text, tables, images, and automatic tables of contents, among
other advantages. 


How to Use This Template
========================

To use this template you must first decide the PDP type. When in doubt, read :ref:`pdp` for details.

Once you've decided which type of PDP yours is going to be, follow the
directions below.

- Make a copy of this file (``.txt`` file, **not** HTML!) or :download:`downloaded here <pdp-template-rst.rst>` and perform
  the following edits.

- Replace the :rst:dir:`sectionauthor` directive with your name, and optionally your
  email address.  Be sure to follow the format carefully: your name
  must appear first, and it must not be contained in parentheses.
  Your email address may appear second (or it can be omitted) and if
  it appears, it must appear in angle brackets.  It is okay to
  obfuscate your email address.

- Change the Service, Function, and Type header to the service applicable to the PDP.

- Change the Title to the title of your PDP.

- Change the Status header to "Draft".

- Change the Service header to the applicable service lie, or "All" if it does not apply to specific service line.

- Change the Function and Type header to one of the functions described in `pdp-meta`.

- Now write your Abstract, Rationale, and other content for your PDP,
  replacing all this gobbledygook with your own text. Be sure to
  adhere to the format guidelines below, specifically on the
  prohibition of tab characters and the indentation requirements.

- Send your PDP submission to the PDP editors.


ReStructuredText PDP Formatting Requirements
============================================

The following is a PDP-specific summary of reStructuredText syntax.
For the sake of simplicity and brevity, much detail is omitted.  For
more detail, see `Resources`_ below.  `Literal blocks`_ (in which no
markup processing is done) are used for examples throughout, to
illustrate the plaintext markup.


General
-------

Tab characters must never appear in the document at all.


Section Headings
----------------

PDP headings must begin in column zero and the initial letter of each
word must be capitalized as in book titles.  Acronyms should be in all
capitals.  Section titles must be adorned with an underline, a single
repeated punctuation character, which begins in column zero and must
extend at least as far as the right edge of the title text (4
characters minimum). Title texts are verline/underline-adorned with "#" (pound signs). First-level section titles are underlined with
"=" (equals signs), second-level section titles with "-" (hyphens),
third-level section titles with "*" (asterisk), fourth-level section titles with "^" (caret), and fifth-level section titles with "'" (single quotes or
apostrophes).  For example::

    *****************************
    Title of PDP (Title Case)
    *****************************

    First-level section (setence case)
    ==================================

    Second-level section
    --------------------

    Third-level section
    *******************

    Fourth-level section
    ^^^^^^^^^^^^^^^^^^^^

    Fifth-level section
    '''''''''''''''''''

You shouldn't have more than five levels of sections in your PDP.  If
you do, you should consider rewriting it.

You must use two blank lines between the last line of a section's body
and the next section heading.  If a subsection heading immediately
follows a section heading, a single blank line in-between is
sufficient.

The body of each section is not normally indented, although some
constructs do use indentation, as described below.  Blank lines are
used to separate constructs.


Paragraphs
----------

Paragraphs are left-aligned text blocks separated by blank lines.
Paragraphs are not indented unless they are part of an indented
construct (such as a block quote or a list item).


Inline Markup
-------------

Portions of text within paragraphs and other text blocks may be
styled.  For example::

    Text may be marked as *emphasized* (single asterisk markup,
    typically shown in italics) or **strongly emphasized** (double
    asterisks, typically boldface).  ``Inline literals`` (using double
    backquotes) are typically rendered in a monospaced typeface.  No
    further markup recognition is done within the double backquotes,
    so they're safe for any kind of code snippets.


Block Quotes
------------

Block quotes consist of indented body elements.  For example::

    This is a paragraph.

        This is a block quote.

        A block quote may contain many paragraphs.

Block quotes are used to quote extended passages from other sources.
Block quotes may be nested inside other body elements.  Use 4 spaces
per indent level.


Literal Blocks
--------------

..  
    In the text below, double backquotes are used to denote inline
    literals.  "``::``" is written so that the colons will appear in a
    monospaced font; the backquotes (``) are markup, not part of the
    text.  See "Inline Markup" above.

    By the way, this is a comment, described in "Comments" below.

Literal blocks are used for code samples or preformatted ASCII art. To
indicate a literal block, preface the indented text block with
"``::``" (two colons).  The literal block continues until the end of
the indentation.  Indent the text block by 4 spaces.  For example::

    This is a typical paragraph.  A literal block follows.

    ::

        for a in [5,4,3,2,1]:   # this is program code, shown as-is
            print a
        print "it's..."
        # a literal block continues until the indentation ends

The paragraph containing only "``::``" will be completely removed from
the output; no empty paragraph will remain.  "``::``" is also
recognized at the end of any paragraph.  If immediately preceded by
whitespace, both colons will be removed from the output.  When text
immediately precedes the "``::``", *one* colon will be removed from
the output, leaving only one colon visible (i.e., "``::``" will be
replaced by "``:``").  For example, one colon will remain visible
here::

    Paragraph::

        Literal block


Lists
-----

Bullet list items begin with one of "-", "*", or "+" (hyphen,
asterisk, or plus sign), followed by whitespace and the list item
body.  List item bodies must be left-aligned and indented relative to
the bullet; the text immediately after the bullet determines the
indentation.  For example::

    This paragraph is followed by a list.

    * This is the first bullet list item.  The blank line above the
      first list item is required; blank lines between list items
      (such as below this paragraph) are optional.

    * This is the first paragraph in the second item in the list.

      This is the second paragraph in the second item in the list.
      The blank line above this paragraph is required.  The left edge
      of this paragraph lines up with the paragraph above, both
      indented relative to the bullet.

      - This is a sublist.  The bullet lines up with the left edge of
        the text blocks above.  A sublist is a new list so requires a
        blank line above and below.

    * This is the third item of the main list.

    This paragraph is not part of the list.

Enumerated (numbered) list items are similar, but use an enumerator
instead of a bullet.  Enumerators are numbers (1, 2, 3, ...), letters
(A, B, C, ...; uppercase or lowercase), or Roman numerals (i, ii, iii,
iv, ...; uppercase or lowercase), formatted with a period suffix
("1.", "2."), parentheses ("(1)", "(2)"), or a right-parenthesis
suffix ("1)", "2)").  For example::

    1. As with bullet list items, the left edge of paragraphs must
       align.

    2. Each list item may contain multiple paragraphs, sublists, etc.

       This is the second paragraph of the second list item.

       a) Enumerated lists may be nested.
       b) Blank lines may be omitted between list items.

Definition lists are written like this::

    what
        Definition lists associate a term with a definition.

    how
        The term is a one-line phrase, and the definition is one
        or more paragraphs or body elements, indented relative to
        the term.


Tables
------

Simple tables are easy and compact::

    =====  =====  =======
      A      B    A and B
    =====  =====  =======
    False  False  False
    True   False  False
    False  True   False
    True   True   True
    =====  =====  =======

There must be at least two columns in a table (to differentiate from
section titles).  Column spans use underlines of hyphens ("Inputs"
spans the first two columns)::

    =====  =====  ======
       Inputs     Output
    ------------  ------
      A      B    A or B
    =====  =====  ======
    False  False  False
    True   False  True
    False  True   True
    True   True   True
    =====  =====  ======

Text in a first-column cell starts a new row.  No text in the first
column indicates a continuation line; the rest of the cells may
consist of multiple lines.  For example::

    =====  =========================
    col 1  col 2
    =====  =========================
    1      Second column of row 1.
    2      Second column of row 2.
           Second line of paragraph.
    3      - Second column of row 3.

           - Second item in bullet
             list (row 3, column 2).
    =====  =========================


Hyperlinks
----------

When referencing an external web page in the body of a PDP, you should
include the title of the page in the text, with either an inline
hyperlink reference to the URL or a footnote reference (see
`Footnotes`_ below).  Do not include the URL in the body text of the
PDP.

Hyperlink references use backquotes and a trailing underscore to mark
up the reference text; backquotes are optional if the reference text
is a single word.  For example::

    In this paragraph, we refer to the `Python web site`_.

An explicit target provides the URL.  Put targets in a References
section at the end of the PDP, or immediately after the reference.
Hyperlink targets begin with two periods and a space (the "explicit
markup start"), followed by a leading underscore, the reference text,
a colon, and the URL (absolute or relative)::

    .. _Python web site: http://www.python.org/

The reference text and the target text must match (although the match
is case-insensitive and ignores differences in whitespace).  Note that
the underscore trails the reference text but precedes the target text.
If you think of the underscore as a right-pointing arrow, it points
*away* from the reference and *toward* the target.

The same mechanism can be used for internal references.  Every unique
section title implicitly defines an internal hyperlink target.  We can
make a link to the Abstract section like this::

    Here is a hyperlink reference to the `Abstract`_ section.  The
    backquotes are optional since the reference text is a single word;
    we can also just write: Abstract_.

Footnotes containing the URLs from external targets will be generated
automatically at the end of the References section of the PDP, along
with footnote references linking the reference text to the footnotes.

Text of the form "PDP x" or "RFC x" (where "x" is a number) will be
linked automatically to the appropriate URLs.


Footnotes
---------

Footnote references consist of a left square bracket, a number, a
right square bracket, and a trailing underscore::

    This sentence ends with a footnote reference [1]_.

Whitespace must precede the footnote reference.  Leave a space between
the footnote reference and the preceding word.

When referring to another PDP, include the PDP number in the body
text, such as "PDP 1".  The title may optionally appear.  Add a
footnote reference following the title.  For example::

    Refer to PDP 1 [2]_ for more information.

Add a footnote that includes the PDP's title and author.  It may
optionally include the explicit URL on a separate line, but only in
the References section.  Footnotes begin with ".. " (the explicit
markup start), followed by the footnote marker (no underscores),
followed by the footnote body.  For example::

    References
    ==========

    .. [2] PDP 1, "PDP Purpose and Guidelines", Warsaw, Hylton
       (http://www.python.org/dev/peps/PDP-0001)

If you decide to provide an explicit URL for a PDP, please use this as
the URL template::

    http://www.python.org/dev/peps/PDP-xxxx

PDP numbers in URLs must be padded with zeros from the left, so as to
be exactly 4 characters wide, however PDP numbers in the text are
never padded.

During the course of developing your PDP, you may have to add, remove,
and rearrange footnote references, possibly resulting in mismatched
references, obsolete footnotes, and confusion.  Auto-numbered
footnotes allow more freedom.  Instead of a number, use a label of the
form "#word", where "word" is a mnemonic consisting of alphanumerics
plus internal hyphens, underscores, and periods (no whitespace or
other characters are allowed).  For example::

    Refer to PDP 1 [#PDP-1]_ for more information.

    References
    ==========

    .. [#PDP-1] PDP 1, "PDP Purpose and Guidelines", Warsaw, Hylton

       http://www.python.org/dev/peps/PDP-0001

Footnotes and footnote references will be numbered automatically, and
the numbers will always match.  Once a PDP is finalized, auto-numbered
labels should be replaced by numbers for simplicity.


Images
------

If your PDP contains a diagram, you may include it in the processed
output using the "image" directive::

    .. image:: diagram.png

Any browser-friendly graphics format is possible: .png, .jpeg, .gif,
.tiff, etc.

Since this image will not be visible to readers of the PDP in source
text form, you should consider including a description or ASCII art
alternative, using a comment (below).


Comments
--------

A comment block is an indented block of arbitrary text immediately
following an explicit markup start: two periods and whitespace.  Leave
the ".." on a line by itself to ensure that the comment is not
misinterpreted as another explicit markup construct.  Comments are not
visible in the processed document.  For the benefit of those reading
your PDP in source form, please consider including a descriptions of
or ASCII art alternatives to any images you include.  For example::

     .. image:: dataflow.png

     ..
        Data flows from the input module, through the "black box"
        module, and finally into (and through) the output module.

The Emacs stanza at the bottom of this document is inside a comment.


Escaping Mechanism
------------------

reStructuredText uses backslashes ("``\``") to override the special
meaning given to markup characters and get the literal characters
themselves.  To get a literal backslash, use an escaped backslash
("``\\``").  There are two contexts in which backslashes have no
special meaning: `literal blocks`_ and inline literals (see `Inline
Markup`_ above).  In these contexts, no markup recognition is done,
and a single backslash represents a literal backslash, without having
to double up.

If you find that you need to use a backslash in your text, consider
using inline literals or a literal block instead.


Habits to Avoid
===============

Many programmers who are familiar with TeX often write quotation marks
like this::

    `single-quoted' or ``double-quoted''

Backquotes are significant in reStructuredText, so this practice
should be avoided.  For ordinary text, use ordinary 'single-quotes' or
"double-quotes".  For inline literal text (see `Inline Markup`_
above), use double-backquotes::

    ``literal text: in here, anything goes!``


Resources
=========

Many other constructs and variations are possible.  For more details
about the reStructuredText markup, in increasing order of
thoroughness, please see:

* `A ReStructuredText Primer`__, a gentle introduction.

  __ http://docutils.sourceforge.net/docs/rst/quickstart.html

* `Quick reStructuredText`__, a users' quick reference.

  __ http://docutils.sourceforge.net/docs/rst/quickref.html

* `reStructuredText Markup Specification`__, the final authority.

  __ http://docutils.sourceforge.net/spec/rst/reStructuredText.html

The processing of reStructuredText PEPs is done using Docutils_.  If
you have a question or require assistance with reStructuredText or
Docutils, please `post a message`_ to the `Docutils-users mailing
list`_.  The `Docutils project web site`_ has more information.

.. _Docutils:
.. _Docutils project web site: http://docutils.sourceforge.net/
.. _post a message:
   mailto:docutils-users@lists.sourceforge.net?subject=PEPs
.. _Docutils-users mailing list:
   http://docutils.sf.net/docs/user/mailing-lists.html#docutils-users

