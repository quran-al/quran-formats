quran-formats
=============

This [repository](https://github.com/quran-al/quran-formats) contains specifications
of file formats for storing Quran texts.  Some of these specifications are
used by the [quran.al](https://quran.al) project, most notably `qtf` and `qmf`.
Anyone using the formats is encouraged contribute to future
developments of these specifications.

Using the works in this repository is not restricted in any way of form so they can be
considered [open standards](http://en.wikipedia.org/wiki/Open_standard),
or [open formats](http://en.wikipedia.org/wiki/Open_format).

The published and used formats are:

* [Quran Text Format](http://github.com/quran-al/quran-formats/blob/master/qtf.md) (QTF) --
  Simple one-line-per-verse format, mostly compatible with the format
  used by [zekr.org](http://zekr.org) and [tanzil.net](http://tanzil.net).
* [Quran Metadata Format](http://github.com/quran-al/quran-formats/blob/master/qmf.md) (QMF) --
  Used for storing meta data about Quran texts, builds on top of the
  [TOML](https://github.com/toml-lang/toml) format.

There are also some formats that are still in draft:

* [Quran LaTeX Format](http://github.com/oqc/qdf/blob/master/qlf.md) (QLF) --
  Subset of the [LaTeX](http://en.wikipedia.org/wiki/LaTeX) document
  markup language, specifically tailored for rich Quranic content (e.g.:
  footnotes, Arabic text, links, headings).
* [Quran Paragraphing Format](http://github.com/oqc/qdf/blob/master/qpf.md) (QPF) --
  Simple one-line-per-verse format for adding paragraphing to Quranic
  texts, especially useful with originals and translations in the QTF
  format (as they lack paragraphs).
* [Quran Binary Format](http://github.com/oqc/qdf/blob/master/qbf.md) (QBF) --
  Fun attempt to create the smallest possbile file containing the
  complete original Quran in the 28-letter Arabic alphabet in which it
  was originally revealed (using 5bit code points).


## Versioning  and backward compatibility

At this point we do not yet specify a version for each format,
but this will likely change. For now all format should be considered
pre-alpha (`0.x.y`). If you are using these formats, please reach
out as that will usher the `1.0` release. 

For all format we try to maintain backward compatible, the version
number of the format will reflect a major version bump whenever a
backwards incompatible change is made (as specified in the
[semver.org](http://semver.org), where this is called "breaking puplic
API).

We also try to keep formats future proof where possible, avoiding the
need to break backward compatibility.

