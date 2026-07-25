---
type: "query"
date: "2026-07-24T03:15:19.379736+00:00"
question: "เทียบการทำงาน และ process ของ การทำ allele typing ของ ont-chinook กับ savont"
contributor: "graphify"
outcome: "useful"
source_nodes: ["run_cluster()", "cluster_reads_by_snpmers()", "align_and_consensus()", "detect_chimeras()", "refine_asv_depths_with_em()", "classify()"]
---

# Q: เทียบการทำงาน และ process ของ การทำ allele typing ของ ont-chinook กับ savont

## Answer

Expanded from original query via graph vocab: [asv, cluster, consensus, snpmer, chimera, abundance, depth, classify, taxonomy]. Savont clusters reads into ASVs using k-mer and SNPmer evidence, generates and quality-filters consensus sequences, filters PCR chimeras, estimates abundance, and optionally assigns microbial taxonomy. It contains no CYP2D6 star-allele or diplotype caller.

## Outcome

- Signal: useful

## Source Nodes

- run_cluster()
- cluster_reads_by_snpmers()
- align_and_consensus()
- detect_chimeras()
- refine_asv_depths_with_em()
- classify()