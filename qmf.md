Quran Metadata Format (QMF)
===========================

A metadata format for Quran texts, part of the [Quran Formats](https://github.com/quran-al/quran-formats).
It can either be embedded in another file format (as per that file format's
specification), or alternatively it can be saved in a standalone file with the `.qmf` extension,
placed alongside the file/directory provides metadata for --
in carrying the same filename (except for the extension).

The format of the metadata is based on two stadards, that are themselves based on
other standards (mainly ISO-, IETF standards and RFCs).  As the data format
a subset of [TOML](https://github.com/toml-lang/toml) is used, which is quite similar to, yet
more advance and well-specified, then the (in)famous `INI` format.


## Example

See the `meta-example.qmf` file for an example that also specifies all
possible keys this file may contain.


## TODO

Provide a full specification instead of refering to an example.
