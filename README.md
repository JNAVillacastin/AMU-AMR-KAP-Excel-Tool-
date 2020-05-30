# AMR-AMU KAP+ Survey Database beta 2.0 ReadME[^1]


## Updates

1. **Improved spreadsheet** design for easy import into **SPSS** and **R**. Has lesser sheets for a cleaner, more navigatable interface.

2. Revised sheets include the **raw_data** sheet, **coded_data** sheet, and **processed_data** sheet. Sheets follow a **database architectural design** that shows how input data is coded, processed, and summarized. [^2]

3. Graphs have been **replaced** with **smart tables** that can automatically sort data. 

4. **Revised codebook** to accomodate both **string** and **numerical** inputs (e.g. medicine names).[^3] Inclusion of  **new codes** such as:
		-**"na"** stands for "no answer", meaning the interviewee cannot answer or does not have an answer. This still counts as data and should not be confused with missing data ("NA")
		-item numbers are coded into the data sheets as such:

>`[category(d,k,a,p,e,c) + item number]_var name (+ var attribute)`
>
>e.g. **k1_antibiotics** 
		
	
6. **renaming** of existing variables such as:
	- presence of AMR laws -> **reach of AMR laws** (since laws could exist but are not communicated/enacted well)
	- Involvement in Farming Community -> **Participation in Farming Community** (since one can be involved de jure but not participate or participate in a lesser degree)


## Recommendations

1) to prevent **questionable research practices** (QRPs)  such as **data peeking** and **HARKING** that might compromise the validity and replicability of our analysis, it would be very advisable to:
	1. collect the data first with a copy of the **raw_data** sheet, and then,
	2.  import the data into the database **AFTER** all of the sample data has been collected

[^1]: This ReadMe is a **draft**. An improved ReadMe with screenshots of  the database and its features is still under development.
[^2]: A screenshot of the database architecture design is included in the email. 
[^3]: Furnished copies of the revised codebook are still under development.
