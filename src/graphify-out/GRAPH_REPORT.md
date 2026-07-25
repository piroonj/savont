# Graph Report - src  (2026-07-24)

## Corpus Check
- cluster-only mode — file stats not available

## Summary
- 733 nodes · 2297 edges · 23 communities
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS · INFERRED: 5 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `e4e49922`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- .new
- Cli
- map_processing.rs
- taxonomy.rs
- alignment.rs
- mapping.rs
- consensus2.rs
- ConsensusBuilder
- merge.rs
- asv_cluster.rs
- types.rs
- QualCompact3
- seeding.rs
- TwinRead
- Vec
- graph.rs
- get_full_alignment
- databases.rs
- sintax.rs
- kmer_comp.rs
- dna_slice_to_u8

## God Nodes (most connected - your core abstractions)
1. `TwinRead` - 69 edges
2. `Cli` - 65 edges
3. `UnitigGraph` - 47 edges
4. `UnitigNode` - 30 edges
5. `Kmer48` - 29 edges
6. `ConsensusSequence` - 25 edges
7. `Database` - 19 edges
8. `get_reasonable_args()` - 18 edges
9. `QualCompact3` - 17 edges
10. `KmerGlobalInfo` - 17 edges

## Surprising Connections (you probably didn't know these)
- `refine_asv_depths_with_em()` --calls--> `find_compatible_candidates()`  [INFERRED]
  alignment.rs → asv_cluster.rs
- `compute_per_sample_depths()` --calls--> `find_compatible_candidates()`  [INFERRED]
  alignment.rs → asv_cluster.rs
- `compute_minimizers()` --calls--> `minimizer_seeds_positions()`  [INFERRED]
  merge.rs → seeding.rs
- `export()` --calls--> `load_fasta_with_needletail()`  [INFERRED]
  merge.rs → taxonomy.rs
- `polish_assembly()` --calls--> `join_circular_ends()`  [INFERRED]
  polishing_mod.rs → polishing/consensus2.rs

## Import Cycles
- None detected.

## Communities (23 total, 0 thin omitted)

### Community 0 - ".new"
Cohesion: 0.06
Nodes (68): OverlapConfig, ReadOverlapEdgeTwin, StdRng, Direction, &'a UnitigEdge, BaseInfo, beam_test_simple(), beam_walk_test_circular() (+60 more)

### Community 1 - "Cli"
Cohesion: 0.06
Nodes (62): BestAlignments, calculate_match_lengths(), calculate_pairwise_similarities(), ChimeraInfo, detect_chimeras(), filter_chimeras(), HashMap, Option (+54 more)

### Community 2 - "map_processing.rs"
Cohesion: 0.09
Nodes (46): Fraction, Lapper, cov_mapping_breakpoints(), create_small_twinol(), depths_at_points(), depths_at_points_interval(), first_last_mini_in_range(), make_test_mapping() (+38 more)

### Community 3 - "taxonomy.rs"
Cohesion: 0.13
Nodes (36): AsvMapping, classify(), collect_best_mappings(), read_feature_table_for_classify(), Option, Path, Result, String (+28 more)

### Community 4 - "alignment.rs"
Cohesion: 0.16
Nodes (28): align_and_consensus(), analyze_pileup_consensuses(), calculate_adjusted_errors(), compute_per_sample_depths(), compute_per_sample_depths_minimap2(), EquivalenceClass, estimate_quality_error_rates(), generate_consensus_pileups() (+20 more)

### Community 5 - "mapping.rs"
Cohesion: 0.13
Nodes (31): Hasher, check_maximal_overlap(), Anchors, compare_twin_reads(), dp_anchors(), find_exact_matches_indexes(), find_exact_matches_indexes_references(), _find_exact_matches_quadratic() (+23 more)

### Community 6 - "consensus2.rs"
Cohesion: 0.17
Nodes (26): Interval, Mutex, OpLenVec, BaseConsensusSimple, circular_join_basic_test(), circular_join_basic_test_fuzzy(), join_circular_ends(), PoaConsensusBuilder (+18 more)

### Community 7 - "ConsensusBuilder"
Cohesion: 0.14
Nodes (15): BaseConsensus, ConsensusBuilder, HomopolymerCompressedSeq, InsertionCounts, ReadCigarIndex, Dna, Eq, FxHashMap (+7 more)

### Community 8 - "merge.rs"
Cohesion: 0.16
Nodes (26): BTreeMap, compute_minimizers(), djb2_hash(), export(), feature_table_from_dir(), fuzzy_merge_table(), read_asv_mapping_keys(), HashMap (+18 more)

### Community 9 - "asv_cluster.rs"
Cohesion: 0.20
Nodes (31): add_read_snpmers_to_index(), add_read_to_bucket_index(), add_read_to_index(), are_consensus_concordant(), assign_read_to_representative(), build_consensus_blockmers(), build_consensus_blockmers_top_n(), build_consensus_snpmers() (+23 more)

### Community 10 - "types.rs"
Cohesion: 0.11
Nodes (27): twin_reads_from_snpmers(), AnchorBuilder, BasePileup, BeamStartState, bioseq_vs_ours(), BlockmerGlobalInfo, BlockmerInfo, CountsAndBases (+19 more)

### Community 11 - "QualCompact3"
Cohesion: 0.11
Nodes (14): Codec, Complement, ComplementMut, H, Hash, Item, Iterator, Ord (+6 more)

### Community 12 - "seeding.rs"
Cohesion: 0.15
Nodes (22): kmer_multiplicity(), polish_assembly(), Vec, blockmer_kmers(), decode(), estimate_sequence_identity(), estimate_sequence_identity_vec(), fmh_seeds() (+14 more)

### Community 13 - "TwinRead"
Cohesion: 0.19
Nodes (8): compare_blockmers(), find_best_representative_iterative(), validate_candidates_with_blockmers(), From, Percentage, convert_from_u64(), Kmer48, TwinRead

### Community 14 - "Vec"
Cohesion: 0.17
Nodes (14): BeamSearchSoln, BubblePopResult, HeavyCutOptions, OverlapAdjMap, retain_vec_indices(), revcomp_u8(), EdgeIndex, FxHashMap (+6 more)

### Community 15 - "graph.rs"
Cohesion: 0.19
Nodes (13): E, BidirectedGraph, BidirectedGraph<N, E>, GraphEdge, GraphNode, orientation_list(), EdgeIndex, FxHashSet (+5 more)

### Community 16 - "get_full_alignment"
Cohesion: 0.24
Nodes (17): AlignmentResult, Gaps, align_seq_to_ref_slice(), align_seq_to_ref_slice_local(), block_size_from_seq(), extend_cigar(), extend_ends_chain(), fmt() (+9 more)

### Community 17 - "databases.rs"
Cohesion: 0.34
Nodes (15): DatabaseDef, download_emu(), download_gg2(), _download_gtdb(), download_silva(), find(), keyword_list(), load_database() (+7 more)

### Community 18 - "sintax.rs"
Cohesion: 0.20
Nodes (12): extract_kmers(), hit_to_classification(), Rng, Option, Path, Result, Self, String (+4 more)

### Community 19 - "kmer_comp.rs"
Cohesion: 0.29
Nodes (12): get_blockmers_inplace_sort(), get_snpmers(), get_snpmers_inplace_sort(), homopolymer_compression(), parse_unitigs_into_table(), retrieve_masked_kmer(), FxHashMap, Kmer64 (+4 more)

### Community 20 - "dna_slice_to_u8"
Cohesion: 0.29
Nodes (7): SeqSlice, dna_seq_to_u8(), dna_slice_to_u8(), quality_seq_to_u8(), quality_slice_to_u8(), Dna, Seq

## Knowledge Gaps
- **6 isolated node(s):** `BaseConsensusSimple`, `BasePileup`, `TigdexOverlap`, `SnpmerHit`, `AnchorBuilder` (+1 more)
  These have ≤1 connection - possible missing edges or undocumented components.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Cli` connect `Cli` to `.new`, `map_processing.rs`, `alignment.rs`, `mapping.rs`, `consensus2.rs`, `asv_cluster.rs`, `types.rs`, `seeding.rs`, `TwinRead`, `get_full_alignment`, `kmer_comp.rs`?**
  _High betweenness centrality (0.163) - this node is a cross-community bridge._
- **Why does `TwinRead` connect `TwinRead` to `.new`, `Cli`, `map_processing.rs`, `alignment.rs`, `mapping.rs`, `consensus2.rs`, `asv_cluster.rs`, `types.rs`, `QualCompact3`, `seeding.rs`, `Vec`, `kmer_comp.rs`, `dna_slice_to_u8`?**
  _High betweenness centrality (0.151) - this node is a cross-community bridge._
- **Why does `QualCompact3` connect `QualCompact3` to `types.rs`, `dna_slice_to_u8`, `TwinRead`, `ConsensusBuilder`?**
  _High betweenness centrality (0.116) - this node is a cross-community bridge._
- **What connects `BaseConsensusSimple`, `BasePileup`, `TigdexOverlap` to the rest of the system?**
  _6 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `.new` be split into smaller, more focused modules?**
  _Cohesion score 0.06452977890616736 - nodes in this community are weakly interconnected._
- **Should `Cli` be split into smaller, more focused modules?**
  _Cohesion score 0.06050228310502283 - nodes in this community are weakly interconnected._
- **Should `map_processing.rs` be split into smaller, more focused modules?**
  _Cohesion score 0.08862745098039215 - nodes in this community are weakly interconnected._