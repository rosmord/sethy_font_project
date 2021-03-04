# hieroglyphic_font
A (still preliminary) project for an opensource hieroglyphic font

## Need for a generic font

JSesh has a quite exhaustive and nice looking (regarding Hieroglyphica-2000) font now, but I feel a secondary font is needed for a number of purposes:

- the design decision for JSesh fonts, with filled areas, and variable-width lines, is typographically richer, but at the same time, it's difficult to design new signs, and even more difficult to ensure a graphical unity ;
- the current status of JSesh fonts makes it possible to use them for publishing purposes ; however, software writers might prefer a font with a clear license.

## Goals and principles

### License

The font shall be distributed under the creative common CC-BY-SA license, which means:

- you can use the font in a free or commercial project; however, the font and its modifications must be distributed under the CC-BY-SA license too. It means that, if you take a sign from the font, create a variant from it, and distribute the result in a software, the modified *signs* must be available for free under the CC-BY-SA license too;
- you must include somewhere in the product the attribution of the font authors;
- you can *modify* the font to suit your needs, and in particular use existing signs as the basis for new signs

### Design decisions

The font should be easy to use in multiple contexts, and easy to modify. In this respect, I will take a different stance from the one I chose for JSesh fonts: the signs will be drawn in SVG, which is a convenient format for hieroglyphs, and for which powerful editors are available, **but** they will be *line-based*. That is, in contrast to normal fonts (opentype) and to JSesh original fonts, they will not use filled areas. 

A sign will be made of strokes (technically, `svg:path`). Only one line-width will be used for the entire font (we might discuss this decision somehow).

### (Future) Content

As this font is currently supposed to be used by JSesh, MdC codes will be used to name the signs. The font will include :

- A folder containing the "official" SVG signs, with a sub-folder by Gardiner category ;
- a folder containing non-standard signs (using the extension mechanism of JSesh, i.e. user personnal codes).
- maybe a bit of software to create a "normal" font from it, in particular, a Unicode-compatible font (some of this software already exists in JSesh code).


