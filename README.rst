===
TSM
===

Twitter Subgraph Manipulator by `Deen Freelon`_

.. _Deen Freelon: dfreelon@gmail.com

In short, TSM is a Python module that contains a few functions for
analyzing Twitter and Twitter-like (i.e., very sparse, directed)
network data. I wrote it for my own research purposes but thought
someone out there might find it useful.


Here are some of the things TSM can do:

- Extract retweets and @-mentions into edgelist format for network
  analysis and visualization
- Partition networks into communities, isolate the N largest
  communities, and identify the most-connected users in each community
- Measure the insularity of network communities (using EI indices) to
  determine the extent to which each looks like an echo chamber
- Measure the overlap between network communities to determine which
  ones interact more and less often
- Get the top retweets in a Twitter dataset and rank them by N of
  retweets and by community
- Track Twitter (or other) communities over time: compute similarity
  scores (weighted or unweighted Jaccard coefficients) for partitioned
  network communities drawn from the same dataset at two different
  time slices
- Discover which nodes bridge which communities
- Find the most-used hashtags in each community
- Find the most-used hyperlinks or web domains in each community


Here's what you need to use TSM:

- ``tsm.py``, the TSM Python module provided here
- ``community3.py``, a version of Thomas Aynaud's Python
  `implementation`_ of the Louvain method of network community
  detection, modified to work with Python 3.x. It's included here with
  TSM.
- `NetworkX`_, a widely-used Python module for general network
  analysis
- `Python`_ 3.x (needed for Unicode support)

.. _implementation: http://perso.crans.org/aynaud/communities/
.. _NetworkX: http://networkx.github.io/
.. _Python: https://www.python.org/


See ``tsm.py`` for a full description of TSM's functions and how to
use them. The module should work as long as NetworkX is installed and
``community3.py`` and ``tsm.py`` are placed in the same directory.
``tsm_test2.py`` contains code examples, but requires raw Twitter data
to function properly (details in the file itself).


I gratefully acknowledge funding support from the US Institute of
Peace in creating this module.
