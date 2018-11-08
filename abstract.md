# Building decentralized indexes for public genomic data to improve access speed and availability

Luiz Carlos Irber Junior
University of California Davis
Population Health and Reproduction
Davis, CA

wort is a database for sourmash signatures, providing APIs to allow
searching public genomic databases for dataset similarity, performing
taxonomic classification of samples and submission of signatures for
inclusion in search indexes. The main goal for wort is to create a
resource that allows permissive improvements without depending on
central coordination, using decentralized web technologies like IPFS
and dat as building blocks.

A sourmash signature are collections of MinHash sketches with the same
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
