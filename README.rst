.. image:: https://img.shields.io/badge/dmtn--179-lsst.io-brightgreen.svg
   :target: https://dmtn-179.lsst.io
.. image:: https://github.com/lsst-dm/dmtn-179/workflows/CI/badge.svg
   :target: https://github.com/lsst-dm/dmtn-179/actions/

#############################################################################################
The ZOGY image differencing kernel and PSF solutions and some practical implementation issues
#############################################################################################

DMTN-179
========

We present the ideal matching kernel and PSF solutions for Gaussian input PSFs in the ZOGY image matching, noise decorrelation and subtraction method. We discuss sources of numerical noise in Fourier-space that can lead to spatially badly bound image artefacts in the difference images.

Links
=====

- Live drafts: https://dmtn-179.lsst.io
- GitHub: https://github.com/lsst-dm/dmtn-179

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-dm/dmtn-179

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
