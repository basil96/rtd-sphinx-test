TikZ Examples
==============

This is awesome!

Based on instructions from `sphinxcontrib-tikz`_ extension and
a Sphinx primer by `Li-Pro.Net`_.

.. _`sphinxcontrib-tikz`:
   https://sphinxcontrib-tikz.readthedocs.io/en/latest/#

.. _`Li-Pro.Net`:
   https://lpn-doc-sphinx-primer.readthedocs.io/en/0.0.5/index.html

Basic example

.. tikz:: [>=latex',dotted,thick] \draw[->] (0,0) -- (1,1) -- (1,0)
   -- (2,0);
   :libs: arrows

.. tikz:: An Example Directive with Caption

   \draw[thick,rounded corners=8pt]
   (0,0)--(0,2)--(1,3.25)--(2,2)--(2,0)--(0,2)--(2,2)--(0,0)--(2,0);

An example role: :tikz:`[thick] \node[blue,draw] (a) {A};
\node[draw,dotted,right of=a] {B} edge[<-] (a);`

Examples of TikZ drawings loaded from files

.. rst-class:: centered
.. tikz:: A classical physics problem
   :include: tikz/physics-problem.tex

.. rst-class:: centered
.. tikz:: Control system principles (PGF/TikZ example)
   :include: tikz/ctrl-loop.tex
   :libs: arrows,shapes
