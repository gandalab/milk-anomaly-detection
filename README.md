# milk-anomaly-detection

Data was processed by kiwi QC and additional removal of tailing G's and adapter sequences with `filterFaultyFastq` script.
Filtered matrix-removed sequences are in MCAW DS `10835051`

Golden datasets to use in analyses:

1. **Kraken genus table using RefSeq DB** (kraken score threshold 0.05): `Kraken_genus_DS10828562.txt` and RPM version `Kraken_genus_RPM_from_DS10828562`
2. **RoDEO on Kraken table** (genus level, P=10, ...): `GenusCounts_allMicrobes_RoDEO_P10.csv`
3. **PRROMenade table using FGP DB** (level 4 pushed-down, using 2020 bact+virus FGP DB, min. match 8 AA): `PRROMenade_table_level4.csv` and raw counts in `PRROMenade_table_raw.csv` [[note additional filtering of filtered reads < 50bp was performed to avoid PRROMenade execution errors]]
4. **RoDEO on PRROMenade table** (parameters...)
5. **HULK k-mer based distance matrix** (k-mer size 21, Jaccard & Weighted Jaccard distances)
6. **TOTAL QC'd read counts** for RPM normalization  (last column "Kraken.UNCLASSIFIED" has the count of quality filtered PhiX filtered read pairs): `Milk66samples_NewFiltering_ReadCounts_forRPM.csv`
