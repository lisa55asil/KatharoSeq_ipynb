# KatharoSeq_ipynb
Setting an objective minimum read count threshold for low biomass 16S rRNA gene amplicon sequencing data using serially diluted mock communities, according to the protocol defined by Minich et al., 2018 (https://msystems.asm.org/content/3/3/e00218-17).


This repository contains an ipython notebook that can be used for 16S rRNA gene amplicon sequencing data to filter out failed samples from a qiime2 feature-table. This process requires:
1. Serially diluted positive controls (e.g. known isolate, commercially available mock community) are included in the experiment
2. The 16S library was created by pooling equal volumes of amplicon (rather than normalizing for equimolar input)

The number of quality filtered reads (which serve as a proxy for biomass in equivolume pooling) is plotted against the percentage of reads that align to the positive control. An allosteric sigmoidal curve is fit, allowing the user to extrapolate how many reads a sample must have to hit a certain threshold in accuracy. This tool does NOT filter out any features, but allows the user to determine which samples should be removed for downstream processing.


