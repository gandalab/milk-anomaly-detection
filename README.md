# milk-anomaly-detection

Data was processed by kiwi QC and additional removal of tailing G's and adapter sequences with `filterFaultyFastq` script
Filtered matrix-removed sequences are in MCAW DS `10835051`

Golden datasets to use in analyses:

1. Kraken table (genus level, using RefSeq DB, kraken score threshold 0.05): `Kraken_genus_DS10828562.txt` and RPM version `Kraken_genus_RPM_from_DS10828562`
2. RoDEO on Kraken table (parameters...)
3. PRROMenade table (level 4 pushed-down, using 2020 bact+virus FGP DB, min. match 8 AA): `PRROMenade_table_level4.csv` and raw counts in `PRROMenade_table_raw.csv`
4. RoDEO on PRROMenade table (parameters...)
5. HULK distance matrix (k-mer size 21, Jaccard & Weighted Jaccard distances)
6. TOTAL QC'd read count table for RPM normalization  (total = low qual + matrix + microbe + unknown)
