# milk-anomaly-detection
## Differential abundance with Songbird

**Summary** This folder contains all data transformations and analysis performed starting with raw read counts with contaminants removed: `read_counts_decontaminated.txt`. The primary dataset was trasformed, imported into Qiime2, Differential Abundance was performed with the Songbird plugin, and visualized with the Qurro plugin.

**Primary Output** **`qurro_plot_cat_baseline.qzv`** should be vizualized in a browser using [view.qiime2.org] (https://view.qiime2.org). If you use the `Autoselecting Features` on the bottom right and pick 5% and hit apply, that will give you the 5% most differentially abundant features for each category using Baseline samples as the reference.
For more information on data analysis and interpretation see the [Songbird Tutorial] (https://github.com/biocore/songbird) and the [Qurro Tutorial] (https://github.com/biocore/qurro#installation-and-usage).

**CodeLog** has the entire analysis commented - if you have any specific questions please refer to that file.


