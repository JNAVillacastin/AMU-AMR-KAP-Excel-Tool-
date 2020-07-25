# AMR-AMU KAP+ Excel Tools v2.0-beta.1 ReadME<sup>1</sup>

## Important Links
1. Tutorial Guide for the KAP+ Excel Tools [https://jnavillacastin.github.io/AMU-AMR-KAP-Excel-Tool-/]
2. Video Tutorials (*under development*)

## Updates

1. **Improved spreadsheet** design for easy import into **SPSS** and **R**. Has lesser sheets for a cleaner, more navigatable interface.

2. Revised sheets include the **raw_data** sheet, **coded_data** sheet, and **processed_data** sheet. Sheets follow a **database architectural design** that shows how input data is coded, processed, and summarized.

3. Graphs have been **replaced** with **smart tables** that can automatically sort data. 

4. **Revised codebook** to accommodate both **string** and **numerical** inputs (e.g. medicine names); inclusion of  **new codes** such as:
		-**"na"** simultaneously stands for "no answer" and "not applicable", meaning the interviewee does not know the answer or does not need to answer a certain question. This still counts as data and should not be confused with missing data ("NA")
		-item numbers are coded into the data sheets as such:

>`[category(d,k,a,p,e,c) + item number]_var name (+ var attribute)`
>
>e.g. **k1_antibiotics** 
		
	
6. **renaming** of existing variables such as:
	- presence of AMR laws -> **reach of AMR laws** (since laws could exist but are not communicated/enacted well)
	- Involvement in Farming Community -> **Participation in Farming Community** (since one can be involved de jure but not participate or participate in a lesser degree)

7. links to **codebook** and **survey sheets** have been embedded in the Excel tools.

## Recommendations

1) to prevent **questionable research practices** (QRPs)  such as **data peeking** and **HARKING** that might compromise the validity and replicability of our analysis, it would be very advisable to:
	1. collect the data first with a copy of the **raw_data** sheet, and then, import the data into the database **AFTER** all of the sample data has been collected, or
	2. indicate your target **sample size** in the intro sheet
