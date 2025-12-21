# Computer Modern Legacy base

This directory contains font sources for generating the OpenType **Computer Modern Legacy** font family.

## computer-modern-legacy-base-cm

The (Adobe/“Postscript”) Type 1 fonts of “Computer Modern” (“CM”) by the American Mathematical Society (AMS),
as found in my version of TeX Live 2025 (last updated late Oct 2025) here:

    /usr/local/texlive/2025/texmf-dist/fonts/type1/public/amsfonts/cm

These fonts are what is used by pdflatex by default, i.e. what ends up in rendered PDFs in that case.

The [official website by the AMS regarding these fonts](https://www.ams.org/publications/type1-fonts)
states the following (retrieved 21 Dec 2025):

> _Effective with the AMSFonts 3.0 distribution, all Type 1 fonts are released
> under the [SIL Open Font License (OFL)](http://scripts.sil.org/OFL)._

The version in the Type 1 font files is `003.002`, which I read as version 3.2.

Note that these fonts are not mathematically equivalent to the original TeX/LaTeX
Computer Modern fonts by Donald E. Knuth, which are defined and rendered via METAFONT.
For example, the cubic Bézier curves used in Type 1 (and also in OpenType fonts)
can only approximate a section of a circle.

## computer-modern-legacy-base-lm

The OpenType fonts of “Latin Modern” (“LM”) by B. Jackowski and J. M. Nowacki
(on behalf of TeX users groups), as found in my version of TeX Live 2025
(last updated late Oct 2025) here:

    /usr/local/texlive/2025/texmf-dist/fonts/opentype/public/lm

These fonts are what is used by LuaLaTeX and XeLaTeX by default,
i.e. what ends up in rendered PDFs in that case.

The [official website](https://www.gust.org.pl/projects/e-foundry/latin-modern)
states the following (retrieved 21 Dec 2025):

> _The Latin Modern fonts are being released under the
> [GUST Font License (GFL)](https://www.gust.org.pl/projects/e-foundry/licenses),
> which is a free license, legally equivalent to the
> [LaTeX Project Public License (LPPL)](http://www.latex-project.org/lppl/),
> version 1.3c or later._

The version of the fonts here is `2.004`, while further updates would a priori
only be of interest for the Computer Modern Legacy font family if they involved
changes to metrics regarding types that are also in Computer Modern.

Note that the glyphs in the LM fonts are often identical to the ones in the
AMS Computer Modern fonts, but there are differences: While the AMS fonts
do apparently strictly reproduce the METAFONT Computer Modern fonts, as far as
technically possible, the LM fonts have changed some things, both in terms
of glyph shapes and metrics, some to help support more languages.

## computer-modern-legacy-base-cm

A font named ad hoc “Raw OpenType Computer Modern”; it is simply what
FontLab 8.4.2 produced when converting the AMS Computer Modern fonts
from Type 1 to OpenType on 6 Dec 2025.

Since the underlying technology for drawing glyphs (cubic Bézier curves)
would the same in Type 1 and OpenType fonts, I am thus far assuming that
the conversion would be practically lossless concerning glyphs and metrics.

In addition to the conversion I have modified the `<name>` table in the
OpenType font, with also a slightly different name to be in accordance
with the license. For example, for `cmr10.pfb` from
(with additional linebreaks in copyrights for legibility)

```xml
<name>
  <namerecord nameID="1" platformID="1" platEncID="0" langID="0x0" unicode="True">
    Computer Modern Med
  </namerecord>
  <namerecord nameID="2" platformID="1" platEncID="0" langID="0x0" unicode="True">
    Regular
  </namerecord>
  <namerecord nameID="4" platformID="1" platEncID="0" langID="0x0" unicode="True">
    CMR10
  </namerecord>
  <namerecord nameID="5" platformID="1" platEncID="0" langID="0x0" unicode="True">
    003.002
  </namerecord>
  <namerecord nameID="6" platformID="1" platEncID="0" langID="0x0" unicode="True">
    CMR10
  </namerecord>
  <namerecord nameID="0" platformID="3" platEncID="1" langID="0x409">
    Copyright (c) 1997, 2009 American Mathematical Society (&lt;http://www.ams.org&gt;),
    with Reserved Font Name CMR10.
  </namerecord>
  <namerecord nameID="1" platformID="3" platEncID="1" langID="0x409">
    Computer Modern Med
  </namerecord>
  <namerecord nameID="2" platformID="3" platEncID="1" langID="0x409">
    Regular
  </namerecord>
  <namerecord nameID="3" platformID="3" platEncID="1" langID="0x409">
    003.002;;CMR10;2025;FL842
  </namerecord>
  <namerecord nameID="4" platformID="3" platEncID="1" langID="0x409">
    CMR10
  </namerecord>
  <namerecord nameID="5" platformID="3" platEncID="1" langID="0x409">
    003.002
  </namerecord>
  <namerecord nameID="6" platformID="3" platEncID="1" langID="0x409">
    CMR10
  </namerecord>
  <namerecord nameID="16" platformID="3" platEncID="1" langID="0x409">
    Computer Modern
  </namerecord>
</name>
```

to

```xml
  <name>
    <namerecord nameID="1" platformID="1" platEncID="0" langID="0x0" unicode="True">
      Raw OpenType Computer Modern Med
    </namerecord>
    <namerecord nameID="2" platformID="1" platEncID="0" langID="0x0" unicode="True">
      Regular
    </namerecord>
    <namerecord nameID="4" platformID="1" platEncID="0" langID="0x0" unicode="True">
      ROTCMR10
    </namerecord>
    <namerecord nameID="5" platformID="1" platEncID="0" langID="0x0" unicode="True">
      003.002
    </namerecord>
    <namerecord nameID="6" platformID="1" platEncID="0" langID="0x0" unicode="True">
      ROTCMR10
    </namerecord>
    <namerecord nameID="0" platformID="3" platEncID="1" langID="0x409">
      Raw automatic conversion using FontLab 8.4.2 to OpenType
      copyright (c) 2025 Alain Stalder (alain@exactphilosophy.net), of Type 1 font:
      Copyright (c) 1997, 2009 American Mathematical Society (&lt;http://www.ams.org&gt;),
      with Reserved Font Name CMR10.
    </namerecord>
    <namerecord nameID="1" platformID="3" platEncID="1" langID="0x409">
      Raw OpenType Computer Modern Med
    </namerecord>
    <namerecord nameID="2" platformID="3" platEncID="1" langID="0x409">
      Regular
    </namerecord>
    <namerecord nameID="3" platformID="3" platEncID="1" langID="0x409">
      003.002;;ROTCMR10;2025;FL842
    </namerecord>
    <namerecord nameID="4" platformID="3" platEncID="1" langID="0x409">
      ROTCMR10
    </namerecord>
    <namerecord nameID="5" platformID="3" platEncID="1" langID="0x409">
      003.002
    </namerecord>
    <namerecord nameID="6" platformID="3" platEncID="1" langID="0x409">
      ROTCMR10
    </namerecord>
    <namerecord nameID="16" platformID="3" platEncID="1" langID="0x409">
      Raw OpenType Computer Modern
    </namerecord>
  </name>
```

Note that I used the word “raw” in the name also to imply that normally
you would  not want to use these fonts directly, even though the glyphs
they contain directly would apparently already be at correct Unicodes,
at least for the text fonts.

Also in this directory are the OpenType fonts rendered to TTX format,
which is a readable “xml” format (see `<name>` tables above for two examples)
that apparently originated from 
[fontTools](https://github.com/fonttools/fonttools),
a library for manipulating fonts, written in Python.

## computer-modern-legacy-base-lm

This directory contains just symlinks to all LM OpenType files,
plus each font also rendered to TTX format here.

