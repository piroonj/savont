---
type: "query"
date: "2026-07-24T23:16:11.756362+00:00"
question: "จากผลของ savont นี้ ไฟล์แต่ละไฟล์ที่อยู่ใน temp เป็นไฟล์ที่มีความหมายว่าอย่างไรบ้าง"
contributor: "graphify"
outcome: "useful"
source_nodes: ["run_cluster()", "cluster_reads_by_kmers()", "cluster_reads_by_snpmers()", "align_and_consensus()", "analyze_pileup_consensuses()", "merge_similar_consensuses()", "refine_asv_depths_with_em()", "classify()"]
---

# Q: จากผลของ savont นี้ ไฟล์แต่ละไฟล์ที่อยู่ใน temp เป็นไฟล์ที่มีความหมายว่าอย่างไรบ้าง

## Answer

Expanded from original query via graph vocab: [cluster, quality, consensus, asv, mapping, kmer, snpmer, merge, polish, abundance, classify, taxonomy]. The temp directory stores checkpoints across Savont stages: kmer_clusters_stage2 and SNPmer cluster files record progressive read clustering; consensus_sequences, low-quality files, and clusters_after_quality_filter_stage4 record initial consensus and quality partitioning; polished_consensuses, final_clusters_merged_stage5, and merged_consensus_sequences record deduplication and merge state before chimera filtering; final_asvs_for_em and read_to_asv_mappings are the candidate reference and diagnostic read mappings used for EM abundance refinement. Final user-facing outputs live above temp: final_asvs.fasta, feature-table.tsv, final_clusters.tsv, taxonomy mappings and abundance tables.

## Outcome

- Signal: useful

## Source Nodes

- run_cluster()
- cluster_reads_by_kmers()
- cluster_reads_by_snpmers()
- align_and_consensus()
- analyze_pileup_consensuses()
- merge_similar_consensuses()
- refine_asv_depths_with_em()
- classify()