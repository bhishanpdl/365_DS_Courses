# Data Processing Tips
- If we have larger dataset, eg > 1GB, do not process all data at once.
- First read only few rows, eg 1000. Look at columns and differentiate numerical columns, discrete columns, date columns, unwanted columns etc.
- Deal each group of columns separately and combine them
  in the end for the data analysis.

# Discrete Variables
- Get woe data frame
- sort values by WOE
- Check number count and woe and group them.
- Make separate category for large number column

# Continuous Variables (fine-classing + coarse-classing)
- If we have about 100 categories, we can see them without binning.
- If more than 100, first categorize the data into fine classing, eg into 50 bins. The category are also called factors.
- Sort them by value, not by WOE
- Again look at number count and woe to make categories.
- Let's say when binning annual income into 50 bins,
  we see large proportion (eg 90%) in bin0, then we need to increase
  the bin number, eg to 100. pd.cut(ser,100)


# WOE Notes
- If we see zigzag woe chart, we should suspect low number of counts
- We can group all low number counts into one single category, or make
  two or three depending how the curve looks.
- If we see monotonically decreasing, its easy to partition, since each patition we have decreasing WOE. Look at zigzag up-down curves take some of them and make a single group.
