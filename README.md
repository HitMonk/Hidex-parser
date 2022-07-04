# Hidex-parser
This project aims to create a parser to collate daily OD measurements from HIDEX microplate reader.\
Will take in multiple outputs from the HIDEX plate reader and convert them into a single excel file with all the daily counts per well/ sample based on selected options. 


The datasets will always be labelled in the following pattern:\
algae_growth_rfu_20220611_084305_124+38+bac.xlsx : Breakdown \
algae_growth_rfu == name of hidex program\
20220611 == date -- this is important as we will have to sort the excel files by the different dates and generate a week long growthcurve
124+38+bac == label/ treatment.

First, we need to collect all the different treatments, then sort the files by date. Each excel file will have data separated by different rows. The title of the rows will show which wells and what measurements are taken.

Sample: This title represents the different wells measured by the HIDEX plate reader. The plate reader can measure 24,48 and 96 well plates. This information can either be explicitly fed by the user or measured by the number of wells labelled under Sample title.

The next few titles can also change, but for the simplicity of this parser lets start with these titles:\
OD(440) -- OD corresponding to the wells measured at 440 nm.\
OD(680) -- OD corresponding to the wells measured at 680 nm.\
OD(600) -- OD corresponding to the wells measured at 600 nm.
