Catalan and German: `apertium-cat-deu`
===============================================================================

This is an Apertium language pair for translating between Catalan and
German. What you can use this language package for:

* Translating between Catalan and German
* Morphological analysis of Catalan and German
* Part-of-speech tagging of Catalan and German

For information on the latter two points, see subheading "For more
information" below.

Requirements
-------------------------------------------------------------------------------

You will need the following software installed:

* lttoolbox (>= 3.3.0)
* apertium (>= 3.3.0)
* vislcg3 (>= 0.9.9.10297)
* apertium-cat
* apertium-deu

If this does not make any sense, we recommend you look at: www.apertium.org.

Compiling
-------------------------------------------------------------------------------

Given the requirements being installed, you should be able to just run:

    $ ./configure
    $ make
    # make install

You can use `./autogen.sh` instead of `./configure` you're compiling from
source. If you installed any prerequisite language packages using a `--prefix`
to `./configure`, make sure to give the same `--prefix` to `./configure` here.

Testing
-------------------------------------------------------------------------------

If you are in the source directory after running make, the following
commands should work:

    $  echo "Hola món!" | apertium -d . cat-deu
    Hallo Welt!

    $ echo "Klein Welt" | apertium -d . deu-cat
    Petit món

After installing somewhere in `$PATH`, you should be able to do e.g.

    $  echo "Hola món!" | apertium cat-deu
    Hallo Welt!

Files and data
-------------------------------------------------------------------------------

* `apertium-cat-deu.cat-deu.dix`  - Bilingual dictionary
* `apertium-cat-deu.cat-deu.t1x`  - Chunking rules for translating into German
* `apertium-cat-deu.deu-cat.t1x`  - Chunking rules for translating into Catalan
* `apertium-cat-deu.cat-deu.t2x`  - Interchunk rules for translating into German
* `apertium-cat-deu.deu-cat.t2x`  - Interchunk rules for translating into Catalan
* `apertium-cat-deu.cat-deu.t3x`  - Postchunk rules for translating into German
* `apertium-cat-deu.deu-cat.t3x`  - Postchunk rules for translating into Catalan
* `apertium-cat-deu.cat-deu.lrx`  - Lexical selection rules for translating into German
* `apertium-cat-deu.deu-cat.lrx`  - Lexical selection rules for translating into Catalan
* `modes.xml`                     - Translation modes

For more information
-------------------------------------------------------------------------------

* http://wiki.apertium.org/wiki/Installation
* http://wiki.apertium.org/wiki/apertium-cat-deu
* http://wiki.apertium.org/wiki/Using_an_lttoolbox_dictionary

Help and support
-------------------------------------------------------------------------------

If you need help using this language pair or data, you can contact:

* Mailing list: apertium-stuff@lists.sourceforge.net
* IRC: `#apertium` on `irc.freenode.net`

See also the file AUTHORS included in this distribution.
