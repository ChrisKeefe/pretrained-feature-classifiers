# Pretrained feature classifier scripts

## Quickstart

1. Run `make clean` to clean up the `outputs` dir.
2. Ensure the database source files are present in their respective subdirs
   in `inputs/gg` and `inputs/silva`. Naming matters. Consult the directory
   listing example, below.
3. Ensure the `FeatureData[Sequence]` Artifact from the Moving Pictures
   tutorial is present in `inputs/validation-tests`, to be used for comparing
   `FeatureData[Taxonomy]` produced by the new classifiers. Consult the
   directory listing example, below.
4. Copy the taxonomies produced during the last classifier-training session from `<prior-session>/outputs/validation-tests` to `inputs/validation-tests`. Note: filenames will need to be changed in the process. Consult the directory listing example,
   below.
5. Run `make all`. GG classifiers should be done in <1hr; Silva <24hrs.

### Proposed directory listing

```
.
├── LICENSE
├── Makefile
├── README.md
├── inputs
│   ├── gg
│   │   ├── 99_otu_taxonomy.txt
│   │   └── 99_otus.fasta
│   ├── silva
│   │   ├── 7_level_taxonomy.txt
│   │   └── silva132_99.fna
│   └── validation-tests
│       ├── gg-13-8-99-expected-515-806-taxonomy.qza
│       ├── gg-13-8-99-expected-taxonomy.qza
│       ├── mp-rep-seqs.qza
│       ├── silva-132-99-expected-515-806-taxonomy.qza
│       └── silva-132-99-expected-taxonomy.qza
├── outputs
│   ├── intermediate
│   ├── logs
│   ├── pretrained-classifiers
│   └── validation-tests
└── train.sh
```
