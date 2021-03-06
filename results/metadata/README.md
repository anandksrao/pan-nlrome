# Explanation of metadata columns

##File 'orthogroup_based_metadata.tsv'
- idnew: Reinspected orthogroup identifier
- nuc.diversity.within
- hap.diversity.within
- Pi
- Tajima.D
- n.segregating.sites
- Rozas.R_2
- Fu.Li.F
- Fu.Li.D
- Fu.F_S
- Strobeck.S
- alnlength
- size
- class: major NLR class in orthogroup
- subclass: major NLR subclass in orthogroup
- cls.per
- ids
- pairs: number of genes that are paired
- branchlength
- edpSel
- pdpSel
- pSelCls
- exp.avg
- exp.dev
- ogtype: orthogroup part of core, shell, or cloud 
- araport11: Araport11 gene member(s) in orthogroup
- expression.strength
- tissue.bias
- pathogen.induction

## File 'accession_metadata.tsv':
- Identifier: numeric accession identifier
- 1001_ecotype: numeric accession identifier from the 1001G project
- Accession: accession name
- Stock_Numbers: seed stock number
- Origin: country of geographic origin
- latitude: exact latitude of geographic origin
- longitude: exact longitude of geographic origin
- Relict: accession belongs (1) or does not belong (0) to the relict group
- MAGIC-founder: accession belongs (1) or does not belong (0) to the group of MAGIC-founders
- Size_Selection: size selection method used. BP=BluePippin; SE=SageElf
- Sequencing_Provider: MPI=Max Planck Institute for Developmental Biology, Tuebingen; UNC=The University of North Carolina at Chapel Hill; EI=Earlham Institute, Norwich 
- Sequencing_Facility
- Library_Adaptors: library adaptors used
- SMRT_cells: number of SMRT cells that produced the dataset
- multiplexed: data was produced multiplexed (1) or not multiplexed (0)
- Population: populations as defined in the 1001G project
- Albugo_AcEx1_phenotype: resistance/susceptibility phenotype to Albugo AcEx1. GS=Green Susceptible; GR=Green Resistant; WCS=Weak Chlorotic Susceptible

## File 'transcript_metadata.tsv':
- Transcript_ID: transcript identifier
- Gene_ID: gene identifier
- Architecture: sorted domain list
- Collapsed_Arch: collapsed and unsorted domain list
- Subclass: subclass an NLR belongs to
- Combined_Subclasses: summarized version of column4 (e.g. for T(N,L)X in col5, col4 contains TLX, TNLX, TNX, and TX)
- Arch_Type: canonical or with integrated domains (noncanonical)
- OG_orig_ID: identifier from initial orthogroup calculations
- OG_orig_Size: from initial orthogroup calculations
- OG: final orthogourp identifier after refinement
- OG_Size: final size after refinement
- Fusion_Flag: from webapollo, points to gene fusion correction
- Merged_Flag: from webapollo, points to gene splitting
- Pair_Flag
- PutPair_Flag
- Truncated_Flag: from webapollo, gene putatively truncated
- Pseudogene_Flag: from webapollo, gene with similarity to pseudogene in Araport11
- NoEvidence_Flag: from webapollo, reannotation done without direct evidence from any webapollo track
- CorBound_Flag: from webapollo, geneboundaries were corrected without direct evidence from Araport11 proteins or transcripts
- CorTrans_Flag: from webapollo, intron/exonboundaries were corrected without direct evidence from Araport11 proteins or transcripts
- Misassembly_Flag: from webapollo, gene on putatively misassembled contig
- Mod_Flag: from webapollo, used if gene model was extensively changed (mostly without evidence from gene predictors or Araport11 transcript/protein mappings) in order to rescue the doma$
- Note_Flag: from webapollo, note present in webapollo
- Accession_Name
- Origin: geographic origin country
- Seed_Collection
- Sequencing_Facility
- Population
- Albugo_Phenotype: GS=Green Susceptible, GR=Green Resistant, WCS=Weak Chlorotic Susceptible
- Assembly_Quality
- Expression
- Relict_Flag
- TE_In_Exons: one or more TE(s) predicted in exon(s)
- TE_In_Introns: one or more TE(s) predicted in intron(s)
- TEs_2kb_Downstream: one or more TE(s) predicted in 2kb region downstream of gene
- TEs_2kb_Upstream: one or more TE(s) predicted in 2kb region upstream of gene
- Outlier: binary; 1=Outlier 0=no-Outlier

## File 'og_other_metadata_discuss.tsv':
- idnew: Reinspected orthogroup identifier
- idold: Original orthogroup identifier
- status: orthogroup or singleton
- use: '0' used for OGs where it was not possible to generate a proper tree during orthogroup refinement because sequence divergence in the transcript alignment was to high or the number of sequences was to low (<4)
- NLRs: number of NLRs contained
- majorclass: major NLR class
- majorsubclass: major NLR subclass
- pairs: number of genes that are in pairs
- putpairs: number of genes that are in putative pairs
- IDs: number of genes with integrated domains
- paralogs_ogold: Paralogs in the original orthogroups (see column idold). Might be 'none', 'simple' (duplications in terminal branches), 'complex' (duplications spread across the whole phylogeny), or 'both' (simple and complex paralogs occur)

## File 'architecture_metadata.tsv'
summarizes domain-architecture based stats and dataset analysis intersections. Below is a brief description of each column content

- Collapsed_Arch: 97 collapsed architectures reverse sorted by the number of NLRs
- Size: Number of transcripts in each collapsed architecture
- Size_ratio: Relative size compared to the total number of NLRs (total: 13160; excludes: renseq-6909, ALYR and CRUB)
- Arch_Type: Architectures containing any combination of Coil/TIR/RPW8/NB/LRR are canonical. Architectures containing any other domain are noncanonical
- ArchType_ratio: Relative size compared to the number of transcript in the correspondent Arch_Type (canonical: 12,496; noncanonical: 664; excl. renseq-6909, ALYR and CRUB)
- Transcript: List of transcript identifiers
- Subclass: Higher-order domain categories in which each domain architecture is included
- Combined_Subclasses: Expanded version of Subclasses, including between parenthesis domains that might be included in each respective subclass
- pair_putpair_size: Number of transcripts flagged as pair or putpair
- pair_putpair_ratio: Relative size of paired/putpaired genes in compared to the total number of genes (13,160; excl. renseq-6909, ALYR and CRUB)
- pair_putpair_transcripts: List of transcript identifiers flagged as pair or putpair
- transcripts_assigned_to_OGs: Number of transcripts assigned to Orthogroups
- Number_different_OGs: Number of different orthogroups to which trnscripts with the same collapsed architecture were assigned to
- transcripts_assigned_to_refinedOGs: Number of transcripts assigned to Refined Orthogroups
- Number_different_refinedOGs: Number of different refined orthogroups to which trnscripts with the same collapsed architecture were assigned to
- Collapsed_Arch_in_Family: (1) Collapsed Architectures detected in Arabidopsis halleri, Arabidopsis lyrata, Camelina sativa, Capsella grandiflora, Capsella rubella, Leavenworthia alabamica, Aethionema arabicum, Thellungiella parvula, Arabis alpina, Sisymbrium irio, Thellungiella halophila, Thellungiella salsuginea, Raphanus sativus, Brassica rapa, Brassica nigra, Brassica napus, Brassica juncea and Brassica oleracea. (0) not detected


## File 'domain_metadata.tsv'
summarizes domain-based stats and dataset analysis intersections\. Below is a brief description of each column content\.

- Domain_ID: Pfam-A domain accessions reverse sorted by the number of NLRs. NB=PF00931, TIR=PF01582, LRR=(PF00560|PF07725|PF13306|PF13855) and RPW8=PF05659. Coil is not a Pfam 
domain and was obtained from majority vote of three Coiled-coils predictors
- Pfam_identifier: Pfam-A domain identifiers mapped from Pfam-A.clans.tsv (ftp://ftp.ebi.ac.uk/pub/databases/Pfam/current_release)
- Pfam_description: Pfam-A domain descriptions mapped from Pfam-A.clans.tsv (ftp://ftp.ebi.ac.uk/pub/databases/Pfam/current_release)
- Interpro_entry: InterPro accession.
- ID: Presence/absence of Integrated domains. (1) Present; (0) Absent.
- Size: Number of transcripts
- Pair/Putpair_Size: Number of transcript flagged as pair or putpair.
- Pair/Putpair_Ratio: Relative size of paired/putpaired genes compared to the total number of genes (13160; excl. renseq-6909, ALYR and CRUB).
- Araport11_NLRs: Number of NLR-coding genes with the corresponding domain in the reference TAIR10/Araport11 Col-0 annotation
- Araport11_Architectures: Number of Collapsed architectures with the corresponding domain in the reference TAIR10/Araport11 Col-0 annotation
- Araport11: Presence/absence in the reference TAIR10/Araport11 Col-0 annotation. (1) Present; (0) Absent.
- Brassicaceae_NLRs: Number of NLR-coding genes with the corresponding domain in Arabidopsis halleri, Arabidopsis lyrata, Camelina sativa, Capsella grandiflora, Capsella 
rubella, Leavenworthia alabamica, Aethionema arabicum, Thellungiella parvula, Arabis alpina, Sisymbrium irio, Thellungiella halophila, Thellungiella salsuginea, Raphanus sativus, Brassica rapa, Brassica nigra, Brassica napus, Brassica juncea and Brassica oleracea.
- Brassicaceae_Architectures: Number of Collapsed architectures with the corresponding domain in Arabidopsis halleri, Arabidopsis lyrata, Camelina sativa, Capsella grandiflora, Capsella rubella, Leavenworthia alabamica, Aethionema arabicum, Thellungiella parvula, Arabis alpina, Sisymbrium irio, Thellungiella halophila, Thellungiella salsuginea, Raphanus sativus, Brassica rapa, Brassica nigra, Brassica napus, Brassica juncea and Brassica oleracea.
- Brassicaceae: Presence/absence in Arabidopsis halleri, Arabidopsis lyrata, Camelina sativa, Capsella grandiflora, Capsella rubella, Leavenworthia alabamica, Aethionema arabicum, Thellungiella parvula, Arabis alpina, Sisymbrium irio, Thellungiella halophila, Thellungiella salsuginea, Raphanus sativus, Brassica rapa, Brassica nigra, Brassica napus, Brassica juncea and Brassica oleracea. (1) Present; (0) Absent.
- At-panNLRome_NLRs: Number of NLR-coding genes with the corresponding domain in the 65 Arabidopsis thaliana-panNLR'ome accessions
- At-panNLRome_Architectures: Number of collapsed architectures with the corresponding domain in the 65 Arabidopsis thaliana-panNLR'ome accessions
- At-panNLRome: Presence/absence in the 65 Arabidopsis thaliana-panNLR'ome accessions. (1) Present; (0) Absent.
- Kroj_et_al._Table_S3: Putative integrated decoy in at least one genome from Kroj et al. New Phytologist 2016. (1) Significant enrichment in NLRs; (0) Not significant Sarris_et_al._TableS14_RightP_lt_0.01: Putative integrated decoys in at least one genome from Sarris et al. BMC Biology 2016. (1) Significant enrichment in NLRs; (0) Not significant