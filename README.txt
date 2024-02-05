EDGE DETECTION OF CORROSIONAL FEATURES, 2024

Methodology and Applications of code are detailed in "Edge Detection of 
Corrosional Features from Atomic Force Microscopy"

Affiliated code reads one csv with listed Atomic Force Microscopy data. 
Data is extracted as set by the "dataextraction" function.

Native square size is set equal to "startingpoint_pre" values. These 
may be adjusted for tuning the proposed method to varying sample sizes. 
The code will run effectively as long as data exists in the input file 
for subsequent iterations of the method.

This code only features three successive iterations of the sobel operator,
though it is feasible to increase iterations by extending the nested-loop, 
or adjusting native square size. Though this code is optimized 
for maxmimizing the analyzed surface of an area while mitigating data 
truncation for AFM specific scans of 90.4μm x 90μm, more localized analyses 
are possible for altering beforementioned parameters. 

Additionally, the original nested-loop has been set to process two different 
native square sizes simultaneously. This may be adjusted by altering the 
column size of "startingpoint_pre" and the range of the initial for-loop
in the nested-loop. 

The output magnitudes are ultimately generated for each native square at
the third iteration of sobel operator application. Values are written to a 
user selected output file.