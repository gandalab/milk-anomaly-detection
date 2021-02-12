# milk-anomaly-detection

Data was processed by kiwi QC and additional removal of tailing G's and adapter sequences ("4x filtered" dataset in MCAW)

Golden datasets to use in analyses:

1. Kraken table (genus level, using RefSeq DB, kraken score threshold used?)
2. RoDEO on Kraken table (parameters...)
3. PRROMenade table (level 4 pushed-down, using 2020 bact+virus FGP DB, min. match 8 AA, not normalized in any way): `PRROMenade_table_level4.csv` [`PRROMenade_table_raw.csv` has counts before pushing to level 4, across all KEGG EC levels]
4. RoDEO on PRROMenade table (parameters...)
5. HULK distance matrix (k-mer size 21, Jaccard & Weighted Jaccard distances)
6. TOTAL QC'd read count table for RPM normalization  (total = low qual + matrix + microbe + unknown)
