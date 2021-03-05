# Sethy Creative Common Font
A (still preliminary) project for an opensource hieroglyphic font

## LICENSE

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

If you decide to contribute to this project, you need to agree with the proposed license.

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

#### Font style ?

This is somehow a problem. I don't believe too much in a *neutral* hieroglyphic font which would fit all time-period. At the same time, I understand that some users of JSesh find some of the current signs too peculiar. Some font designers, and in particular the earliest ones, with the Theinhardt font, chose Saite examples, which are a relatively good middle ground. In a completely unscientific attitude, I would tend to choose New Kingdom signs as a basis however. In any case, for the **main** font, the signs characteristics should be chosen in order to be as *typical* as possible.

It also means that taking an actual glyph occurrence as the basis for drawing a sign is possible, but that the final font signs will probably be somehow artificial, with irrelevant details *removed* from the drawing.

One might also consider providing secondary fonts, more rooted in a time-frame (old/middle/new-kingdom, late-period, Ptolemaic and Roman) ;
They would be stored in different folders.


### (Future) Content

As this font is currently supposed to be used by JSesh, MdC codes will be used to name the signs. The font will include :

- A folder containing the "official" SVG signs, with a sub-folder by Gardiner category ;
- a folder containing non-standard signs (using the extension mechanism of JSesh, i.e. user personnal codes).
- maybe a bit of software to create a "normal" font from it, in particular, a Unicode-compatible font (some of this software already exists in JSesh code).


## Workflow and questions

I'm currently looking for a style, and trying to make my mind on a number of problems.

Basically, drawing signs might involve two approaches:

- drawing a sign from a facsimile;
- given a sign description, build a reasonable *artificial* rendering of the sign.

For a font, the second attitude can't be avoided. If you collect random signs from various sources, and use facsimile, you will end up with a weird looking collection of signs you won't be able to mix.

So, at some point, existing signs will be the source for *at least* some parts of new signs. Which doesn't preclude the need to build a good documentation for the signs.

Now, there are also *font-related* problems. A very detailled sign rendering might be fine, but it will probably render poorly in an actual font.

### Case Study A : A1 sign

I start from a *fac-simile* I have made from KV 17:

![A1 fac simile](./facsimile/kv17/rosmorduc_1/A1_KV17_Room J EW.svg)

