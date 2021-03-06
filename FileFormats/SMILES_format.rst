.. _SMILES_format:

SMILES format (smi, smiles)
===========================

**A linear text format which can describe the connectivity and chirality of a molecule**

Open Babel implements the `OpenSMILES specification <http://opensmiles.org>`_.

It also implements an extension to this specification for radicals.

Note that the ``l <atomno>`` option, used to specify a "last" atom, is
intended for the generation of SMILES strings to which additional atoms
will be concatenated. If the atom specified has an explicit H within a bracket
(e.g. ``[nH]`` or ``[C@@H]``) the output will have the H removed along with any
associated stereo symbols.

.. seealso::

  The :ref:`Canonical_SMILES_format` produces a canonical representation
  of the molecule in SMILES format. This is the same as the ``c`` option
  below but may be more convenient to use.



Write Options
~~~~~~~~~~~~~ 

-a  *Output atomclass like [C:2], if available*
-c  *Output in canonical form*
-U  *Universal SMILES*
-I  *Inchified SMILES*
-h  *Output explicit hydrogens as such*
-i  *Do not include isotopic or chiral markings*
-n  *No molecule name*
-r  *Radicals lower case eg ethyl is Cc*
-t  *Molecule name only*
-x  *append X/Y coordinates in canonical-SMILES order*
-C  *'anti-canonical' random order (mostly for testing)*
-o <ordering>  *Output in user-specified order*

     Ordering should be specified like 4-2-1-3 for a 4-atom molecule.
     This gives canonical labels 1,2,3,4 to atoms 4,2,1,3 respectively,
     so that atom 4 will be visited first and the remaining atoms
     visited in a depth-first manner following the lowest canonical labels.
-F <atom numbers>  *Generate SMILES for a fragment*

     The atom numbers should be specified like "1 2 4 7".
-R  *Do not reuse bond closure symbols*
-f <atomno>  *Specify the first atom*

     This atom will be used to begin the SMILES string.
-l <atomno>  *Specify the last atom*

     The output will be rearranged so that any additional
     SMILES added to the end will be attached to this atom.

