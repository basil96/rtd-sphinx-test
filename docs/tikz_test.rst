TikZ Examples
=============

This is awesome!

It is widely known that you can use TeX in Sphinx
documentation to create mathematical formulas. However, it is also
possible to create excellent vector graphics directly in Sphinx!
This means you no longer need to create your vector illustrations in
external software, export them to SVG or PNG, include them with the
rest of the assets in the documentation system, etc. Let Sphinx do
the work for you.

The main advantages are:

1. Out-of-the-box support for `PGF/TikZ`_ via the Sphinx
   extension `sphinxcontrib-tikz`_.
2. Need to modify an illustration? No problem, just edit its code
   directly in the documentation text and rebuild.
3. Plaintext-based system: easy to control revisions via your
   favorite VCS.
4. Integrates easily and flawlessly with `Read The Docs`_.

Based on instructions from `sphinxcontrib-tikz`_ extension and
a Sphinx primer by `Li-Pro.Net`_.

.. _`sphinxcontrib-tikz`:
   https://sphinxcontrib-tikz.readthedocs.io/en/latest/#

.. _`Li-Pro.Net`:
   https://lpn-doc-sphinx-primer.readthedocs.io/en/0.0.5/index.html

.. _`PGF/TikZ`:
   https://en.wikipedia.org/wiki/PGF/TikZ

.. _`Read The Docs`:
   https://readthedocs.org/

Inline Examples
---------------

Basic example:

.. tikz:: [>=latex',dotted,thick] \draw[->] (0,0) -- (1,1) -- (1,0)
   -- (2,0);
   :libs: arrows

The obligatory ubiquitous example, with caption:

.. tikz:: An Example Directive with Caption

   \draw[thick,rounded corners=8pt]
   (0,0)--(0,2)--(1,3.25)--(2,2)--(2,0)--(0,2)--(2,2)--(0,0)--(2,0);

An example inline role: :tikz:`[thick] \node[blue,draw] (a) {A};
\node[draw,dotted,right of=a] {B} edge[<-] (a);`

Examples of TikZ drawings loaded from files
-------------------------------------------

Classical physics: a free-body diagram

.. rst-class:: centered
.. tikz:: A classical physics problem
   :include: tikz/physics-problem.tex

Control systems: a basic diagram

.. rst-class:: centered
.. tikz:: Control system principles (PGF/TikZ example)
   :include: tikz/ctrl-loop.tex
   :libs: arrows,shapes

Drawing demo by author of the package ``tikz-3dplot`` [`source`_]

.. rst-class:: centered
.. tikz:: Demo of tikz-3dplot
    :include: tikz/the-3dplot-package.tex

.. _`source`:
    https://texample.net/tikz/examples/the-3dplot-package/

3D Cube 1 (plain TikZ)

.. rst-class:: centered
.. tikz:: Cube in 3D (without view transform)
    :include: tikz/cube1.tex

3D Cube 2 (drawn using ``tikz-3dplot``)

.. rst-class:: centered
.. tikz:: Cube in 3D (after view transform)
    :include: tikz/cube2.tex

Spherical Polar coordinate system (drawn using ``tikz-3dplot``)

.. rst-class:: centered
.. tikz:: Spherical polar coordinate system
    :include: tikz/cs-spherical-polar.tex

Spherical Elevation coordinate system (drawn using ``tikz-3dplot``)

.. rst-class:: centered
.. tikz:: Spherical elevation coordinate system
    :include: tikz/cs-spherical-elevation.tex
