# VBA Stock Analysis

## Purpose and Overview
Steve is looking to efficiently use an Excel workbook macro to analyze the total volume and growth of various stock data from the years 2017 and 2018. Using a previously written VBA script for this task, we will refactor the code with the use of arrays to determine whether or not the VBA script can be run faster.

## Results
[Excel Workbook with refactored VBA script in AllStocksAnalysisRefactored()](https://github.com/rptseng/stock-analysis/blob/main/VBA_Challenge.xlsm)
### Original Script Run Time
The original script before refactoring with arrays had a run time of 0.901 seconds for the year "2017" 0.905 seconds for the year "2018".

![VBA_2017_Original_Run_Time](https://github.com/rptseng/stock-analysis/blob/main/Resources/VBA_Challenge_2017_old_code_run.png)![VBA_2018_Original_Run_Time](https://github.com/rptseng/stock-analysis/blob/main/Resources/VBA_Challenge_2018_old_code_run.png)

### Refactored Script Run Time
The refactored script had a run time of 0.192 seconds for the year "2017" and 0.187 seconds for the year "2018". On both runs, the refactored code compared to the original code was faster by roughly 0.7 seconds.

![VBA_2017_Refactored_Run_Time](https://github.com/rptseng/stock-analysis/blob/main/Resources/VBA_Challenge_2017.png)![VBA_2017_Refactored_Run_Time](https://github.com/rptseng/stock-analysis/blob/main/Resources/VBA_Challenge_2018.png)

## Summary
1. What are the advantages or disadvantages of refactoring code?

When refactoring code, there is opportunity to improve the existing code to be more easily readable, run faster, and be scalable towards other tasks. The goal is to achieve savings of time and money in the future by cleaning up inefficiencies that may act as obstacles as a project develops.

The disadvantages of refactoring code are that it costs resources to reorganize and maintain without delivering any functional enhancements. There is also a risk of creating unintended or unexpected bugs to the live build if testing is not performed thoroughly.

2. How do these pros and cons apply to refactoring the original VBA script?

In this exercise, the subroutine "AllStocksAnalysisRefactored()" improves in run time over "AllStocksAnalysis()" by not requiring the macro to activate and reference data from the yearValue worksheet on each iteration of the loop. Instead, "AllStocksAnalysisRefactored()" outputs the stock data into the arrays of "tickerVolumes", "tickerStartingPrices", and "tickerEndingPrices" which are iterated entirely on the "AllStocksAnalysis" worksheet to populate the cells with the values.


