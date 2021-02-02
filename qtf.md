Quran Text Format (QTF)
=======================

File format for Quran texts that uses plain text internally: one line per verse,
delimited by a `\n` or `0x0A` (newline or line feed), contains no unnumbered bismallahs,
and is UTF-8 encoded.
Verse numbers are implicit in this format, they can be derived from the line number count.
All chapters simply follow one after another in a single file.

The extension for this format is `.qtf`.

It is based upon the "Text" format that [tanzil.net](http://tanzil.net) and
[zekr.org](http://zekr.org) use; and extends on that basis by having a strict
definition (this document) and allowing metadata to be embedded.

For a more sophisticated format see the **Quran Latex Format**.
The QLF has much more features, including: more markup, ref based footnotes, in-verse line breaks and headings.


## Markup

Markup may be provided with HTML tags. The following HTML tag are allowed:

* `b` — for bold text
* `i` — for italic text (using `em` is not allowed)
* `u` — for underlined text
* `br` — for line breaks

More allow tags are to be expected.


## Headers, commentary, footnotes and/or tafsir

One could fill a QTF file with commentary: the commentary to each verse on its
own line.

Alternatively commentaty/footnotes or even headers could be combined with a text
by using the double bracket (`[[ ... ]]`) notation. If a verse starts with a piece of text
surrounded by double brackets, then that is considered the header.
If a verse ends with a piece of text in double brackets it is considered a 
footnote of commentary.

For example (all on a single line):

    [[The Quran is Detailed in Knowledge]] We have brought them a book which
    We have detailed with knowledge; a guide and a mercy to those who
    acknowledge.[[See 11:1.]]


## Metadata

QTF allows metadata to be embedded, by appending it to the end of the file.
The reason for appending it (instead of putting it at the start of the file) are:

1. the bismallah thereby is still on the first line of the file, and
2. the line numbers can still be used to derive the chapter and verse numbers from.

Metadata may also be provided in a separate file.

The metadata may follow the **Quran Metadata Format**.

For example:

    [...]
    Say, "I seek refuge in the Lord of the people,
    The King of the people,
    The god of people,
    From the evil of the sneaky whisperer,
    Who whispers into the chests of the people,
    From among the Jinn and people."
    ---
    title = "Quran: A Reformist Translation"
    text_type = "translation"
    translators_english = ["Edip Yüksel", "Layth Saleh al-Shaiban", "Martha Schulte-Nafeh"]
    publisher_english = "Rainbow Press"
    date = 2007
    isbn = "978-0979671500"



## VERSION

* `0.0.2` -- Remove the compression feature, and speficy metadata to be embedded.
* `0.0.1` -- Initial release.
