## Data Description

Golden datasets to use in analyses:

### Microbe Tables
1. **Raw read counts with contaminants removed:** `read_counts_decontaminated.txt`  
2. **RPM with contaminants removed, all samples, no RPM threshold** `milk_all_samples_decontam_RPM_DS10828562.txt`
3. **RPM with contaminants removed, supported only (RPM > 0.1)** milk-real-samples-decontam-RPM-supported-microbes-only_from_DS10828562.txt
4. **TOTAL QC'd read counts** for RPM normalization  (last column "Kraken.UNCLASSIFIED" has the count of quality filtered PhiX filtered read pairs): `Milk66samples_NewFiltering_ReadCounts_forRPM.csv`

### Comparative Aanalyses
1. **RoDEO on Kraken table** (genus level, P=10, I=100, R=10^7): `GenusCounts_allMicrobes_RoDEO_P10.csv`
2. **PRROMenade table using FGP DB** (level 4 pushed-down, using 2020 bact+virus FGP DB, min. match 8 AA, features first scaled by total sum and summed per pair, filtering of rare features): `PRROMenade_level4_8AA.csv` [[note1: does not include the large kefir sample; note2: additional filtering of filtered reads < 50bp was performed to avoid PRROMenade execution errors]]
3. **RoDEO on PRROMenade table** (PRROMenade level4 on FGP DB, P=10, I=100, R=10^7): `PRROMenade_L4AA8_RoDEO_P10.csv`
4. **HULK k-mer based distance matrix** (pre-filtered low complexity reads with PRINSEQ -lc_threshold 70, HULK k-mer size 21, Jaccard & Weighted Jaccard distances): `HULK_ent_jaccard_k21.csv` and `HULK_ent_wjaccard_k21.csv`[[note: does not include controls or kefir]]



