# Building decentralized indexes for public genomic data

[Luiz Carlos Irber Júnior](https://github.com/luizirber)

- Department of Population Health and Reproduction, University of California, Davis, USA

Poster presented at [Biological Data Science 2018][1].

## Abstract

wort is a database for sourmash signatures, providing APIs to allow
searching public genomic databases for dataset similarity, performing
taxonomic classification of samples and submission of signatures for
inclusion in search indexes. The main goal for wort is to create a
resource that allows permissive improvements without depending on
central coordination, using decentralized web technologies like IPFS
and dat as building blocks.

A sourmash signature is a collection of MinHash sketches with the same
original dataset but distinct parameters. A MinHash sketch is a data
structure that allows fast similarity estimates for datasets, first
used by Mash with genomic data. In sourmash we extended MinHash
sketches to take the complexity of the dataset into account and avoid
configuration fatigue.

These signatures are most useful when there are many of them available,
especially from public genomic databases like RefSeq or the SRA.
sourmash also includes a Sequence Bloom Tree implementation for
indexing MinHashes, allowing both searching for similarity and
taxonomic classification of datasets. But there is no functionality to
make it easier to share these indexes, and it is up to the user to send
these sketches around or build their own indexes.

wort also aims to explore data locality on networks to overcome the
bandwidth limitations in centralized databases, and move data
preprocessing into web browsers using Webassembly to allow novel
solutions where the user data doesn't need to leave their computers to
be able to participate in the ecosystem.

It is available at https://wort.oxli.org

## Table of Contents

- [Introduction](01.intro.md)
- [sourmash signatures](02.sourmash.md)
- [Current architecture](03.current_arch.md)
- [wort](04.wort.md)
- [Future work](05.future.md)
- [References](#references)
- Appendices
  - [Submitted abstract](abstract.md)
  - [The final poster](poster/poster.pdf)

## References

- Benet, Juan. 2014. “IPFS - Content Addressed, Versioned, P2P File System.” arXiv:1407.3561 [Cs], July. http://arxiv.org/abs/1407.3561.
- Broder, Andrei Z. 1997. “On the Resemblance and Containment of Documents.” In Compression and Complexity of Sequences 1997. Proceedings, 21–29. IEEE. http://ieeexplore.ieee.org/abstract/document/666900/.
- Ogden, Maxwell. n.d. “Dat - Distributed Dataset Synchronization And Versioning.”. [doi:10.31219/osf.io/nsv2c](https://doi.org/10.31219/osf.io/nsv2c).
- Ondov, Brian D., Todd J. Treangen, Páll Melsted, Adam B. Mallonee, Nicholas H. Bergman, Sergey Koren, and Adam M. Phillippy. 2016. “Mash: Fast Genome and Metagenome Distance Estimation Using MinHash.” Genome Biology 17: 132. [doi:10.1186/s13059-016-0997-x](https://doi.org/10.1186/s13059-016-0997-x).
- Solomon, Brad, and Carl Kingsford. 2016. “Fast Search of Thousands of Short-Read Sequencing Experiments.” Nature Biotechnology 34 (3): 300–302. [doi:10.1038/nbt.3442](https://doi.org/10.1038/nbt.3442).
- Torre, Denis, Alexander Lachmann, and Avi Ma’ayan. 2018. “BioJupies: Automated Generation of Interactive Notebooks for RNA-Seq Data Analysis in the Cloud.” BioRxiv, June, 352476. [doi:10.1101/352476](https://doi.org/10.1101/352476).
- Titus Brown, C., and Luiz Irber. 2016. “sourmash: A Library for MinHash Sketching of DNA.” The Journal of Open Source Software 1 (5). [doi:10.21105/joss.00027](https://doi.org/10.21105/joss.00027).

[1]: https://meetings.cshl.edu/meetings.aspx?meet=DATA&year=18
