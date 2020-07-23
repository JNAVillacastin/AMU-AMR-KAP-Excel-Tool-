<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>KAP+ Excel Tool Tutorial</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__left">
    <div class="stackedit__toc">
      
<ul>
<li><a href="#amramu-kap-tool-tutorial">AMR/AMU KAP+ TOOL TUTORIAL</a>
<ul>
<li>
<ul>
<li></li>
</ul>
</li>
<li><a href="#tldr">tl;dr</a></li>
</ul>
</li>
<li><a href="#introduction">Introduction</a>
<ul>
<li><a href="#how-does-the-excel-tool-work">How does the Excel tool work?</a></li>
<li><a href="#parts-of-the-excel-tool">Parts of the Excel Tool</a></li>
<li><a href="#getting-around-the-intro-sheet">Getting around the intro sheet</a></li>
</ul>
</li>
<li><a href="#chapter-1.-data-table-sheet-layout">Chapter 1. Data Table Sheet Layout</a>
<ul>
<li><a href="#indicator-rows">Indicator Rows</a></li>
<li><a href="#observation-rows">Observation rows</a></li>
</ul>
</li>
<li><a href="#chapter-2.-data-table-sheet-functions">Chapter 2. Data Table Sheet Functions</a>
<ul>
<li><a href="#raw_data">raw_data</a></li>
<li><a href="#coded_data">coded_data</a></li>
<li><a href="#processed_data">processed_data</a></li>
</ul>
</li>
<li><a href="#chapter-3.-summary-sheets-layout-and-function">Chapter 3. Summary Sheets Layout and Function</a>
<ul>
<li><a href="#survey_answers">survey_answers</a></li>
<li><a href="#summary">summary</a></li>
<li><a href="#correlation">correlation</a></li>
</ul>
</li>
<li><a href="#chapter-4.-adding-and-updating-the-data-sheets">Chapter 4. Adding and Updating the data sheets</a>
<ul>
<li><a href="#adding-data-to-raw_data">Adding data to raw_data</a></li>
<li><a href="#updating-coded_data-and-processed_data">Updating coded_data and processed_data</a></li>
</ul>
</li>
<li><a href="#chapter-5.-exporting-to-.csv">Chapter 5. “Exporting” to .csv</a></li>
</ul>

    </div>
  </div>
  <div class="stackedit__right">
    <div class="stackedit__html">
      <h1 id="amramu-kap-tool-tutorial">AMR/AMU KAP+ TOOL TUTORIAL</h1>
<p>Glova, N., &amp; Villacastin, J.N.</p>
<hr>
<h4 id="about-this-version">About this version</h4>
<ul>
<li>a short series of video tutorials are currently under development</li>
<li>this is for the <strong>v2.0-beta versions</strong> of the Excel tool</li>
<li>all data shown are dummy data</li>
</ul>
<h2 id="tldr">tl;dr</h2>
<p><strong>What is this tool for?</strong></p>
<ul>
<li>The KAP+ Excel tool is meant for easy data encoding, cleaning, and exploratory analysis.</li>
</ul>
<p><strong>Can I add new observations in the raw_data table?</strong></p>
<ul>
<li>Yes, the tool can be updated with new observations; some function dragging is required to update coded and processed data sheets. Moreover, there is no limit as to how many observations can be added.</li>
</ul>
<p><strong>Do I need to tweak the Excel tool’s functions to update other tables?</strong></p>
<ul>
<li>No, raw data is automatically coded and processed based on the coding scheme in the KAP+ survey sheets. You just need to drag some cell functions in the <strong>coded_data</strong> and <strong>processed_data</strong> sheets  (Please see tutorial below).</li>
</ul>
<p><strong>Can I copy the data in the tool into other spreadsheet formats?</strong></p>
<ul>
<li>Yes, data table sheets in the tool are designed to be easily copied and exported into .csv files for more robust statistical and computational analyses. However, you will have to copy the data sheets you want to use manually (Please see tutorial below).</li>
</ul>
<h1 id="introduction">Introduction</h1>
<p>This is a tutorial guide for the AMU/AMR KAP+ Excel Tool, which is designed to accompany surveyors in the field.</p>
<p>The tool is designed for light <em>exploratory data analysis</em>, but its data tables are designed to be compatible (and efficient) with more robust statistical programming languages/software such as SPSS, SQL, R etc.</p>
<p>However, the naming conventions are optimized for data wrangling in the “tidyverse” R package.<sup class="footnote-ref"><a href="#fn1" id="fnref1">1</a></sup></p>
<h2 id="how-does-the-excel-tool-work">How does the Excel tool work?</h2>
<p>In a nutshell, the Excel tool automatically codes, processes, and analyzes raw data. Survey data is manually inputted with the corresponding codebook answers in the <strong>raw_data</strong> sheet.</p>
<p>Data in the <strong>raw_data</strong> sheet are automatically coded into their corresponding numerical codes in the <strong>coded_data</strong> sheet.</p>
<p>Coded data is summarized both as individual items in the <strong>survey_answers</strong> sheet and as variables in the <strong>processed_data</strong> sheet.</p>
<p>The variable scores in the latter are further processed into parameters in the <strong>summary</strong> sheet and tested for significant correlations in the <strong>correlations</strong> sheet.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3eVClxqfgkT2B5Q9GdcDuZx7UT4Es_t408dZpr-idW_yoJ6h3iBzSWite40z11UjrXTMQn1tp19wlBblGYj8Qh66So1tGOsqvtQPpHSxBJaq6vqzzZj9TWWvpl-6dDA_TbYJ4nhm2dJSF9L0uovb_rj=w749-h565-no?authuser=0" alt="enter image description here"><br>
<sub>Fig.</sub> <sub>1.</sub> <sub>Diagram</sub> <sub>showing</sub> <sub>how</sub> <sub>data</sub> <sub>is</sub> <sub>coded</sub><sub>,</sub> <sub>processed</sub><sub>,</sub> <sub>and</sub> <sub>analyzed</sub> <sub>in</sub> <sub>the</sub> <sub>Excel</sub> <sub>tool</sub></p>
<h2 id="parts-of-the-excel-tool">Parts of the Excel Tool</h2>
<p>The Excel tool contains three parts:</p>
<ol>
<li>The <strong>intro</strong> sheet which contains metadata and links to the codebook, survey sheets, and GitHub repository;</li>
<li><strong>Data table sheets</strong> composed of the <strong>raw_data</strong>, <strong>coded_data</strong>, and <strong>processed_data</strong> sheets; contains data tables/frames in string, code, and processed formats respectively and can be imported into .csv for more robust data analysis; and</li>
<li><strong>Summary sheets</strong> composed of the <strong>survey_answers</strong>, <strong>summary</strong>, and <strong>correlation</strong> sheets; contains exploratory data analyses of the data in the data table sheets.</li>
</ol>
<h2 id="getting-around-the-intro-sheet">Getting around the intro sheet</h2>
<p>Before using the Excel tool to input data or do some analysis, the first sheet you are going to see is the <strong>intro</strong> sheet. Make sure to check the links in the sheet and fill up the metadata portions.</p>
<h3 id="a.-metadata">A. Metadata</h3>
<p>When compiling all the survey data after the survey period, we will be creating an online database (preferably in a cloud-based SQL server) to keep all the data for more robust analyses and meta-analyses. That is why metadata information will be very important. You can input your metadata in the <em>survey information</em> box like the one shown below.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3dBo1F4jcnXt6qMBtRgPhgP03MvOf1XeTDNrUu-wcCtvPNZRRGumyRc3W4wT-JMb448PBuuWzgH2Bs71JUigrfpAKsZF-Hvnr6lpjFXmQU6c1fkZmgrK7VNBGI25pvzswD1sWOg7ADVKIjyTiAmGEQK=w674-h181-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>2</sub><sub>.</sub> <sub>survey</sub> <sub>information</sub> <sub>box</sub><sub>.</sub> <sub>Sample</sub> <sub>size</sub> <sub>automatically</sub> <sub>updates</sub> <sub>upon</sub> <sub>entering</sub> <sub>ID</sub> <sub>numbers</sub> <sub>in</sub> <sub>the</sub> <sub>raw</sub><sub>_</sub><sub>data</sub> <sub>sheet</sub><sub>.</sub></p>
<h3 id="b.-links-to-documents-and-github-repository">B. Links to documents and GitHub repository</h3>
<p>The Excel tool requires that you have a copy of the <em>codebook</em> companion for the <strong>raw_data</strong> sheet and the <em>survey sheets</em> themselves. You can download them in the <em>related documents</em> box as shown below.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3cQKmMG1qXaqSgQ0FMq0dq7vpNRm11ixbmp2e9eWgtRAAFGHWWmsdBRJdbhhV1Ejwji5OyzZauBfmhvUIK--kNX-pTgixp7ZRSjpGD-lWSsE3JvdToe-P6pm0FjCyrBIzhPt2uRg1jksMdTwWxgo28H=w682-h97-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>3.</sub> <sub>Links</sub> <sub>to</sub> <sub>related</sub> <sub>documents</sub><sub>.</sub><br>
Moreover, to check the latest updates of the Excel tool, some demo analyses with R, and other necessary files, you can access them in the GitHub repository as shown below.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3e4khvajoo4NsLLrOCCwginkmDcPOucc28tg8tCnxBRoAmqw_AhG0RT1pv9xfhSjI46_oH_TERrBANjvcNghd8gECpNozl1LtOrVO5EiqwoQxHY_VHi5hz7iucVozBMQmUf1GllkRzPQTD7Wamln82r=w1176-h34-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>4.</sub> <sub>Link</sub> <sub>to</sub> <sub>the</sub> <sub>GitHub</sub> <sub>repository</sub><sub>.</sub></p>
<h3 id="c.-links-to-the-excel-tool-sheets">C. Links to the Excel tool sheets</h3>
<p>You can automatically access the <strong>data table</strong> sheets and the <strong>summary</strong> sheets by clicking on the hyperlinks in the <em>results</em> box as shown below.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3fEU5YR9EJ7P2HqdVndh1uUK39V-c-0RWOF98glnCwoBqs5y_nICl5Ae8MfUJ6N-9geLeQe0kofkdnrbR6T0XBQxAnA6FiOnJTc52V3tr3vxH99Ky_tOZLVYdiFDJpWza28AiFuwoHghpXw28ADIxjz=w511-h271-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>5.</sub> <sub>Links</sub> <sub>to</sub> <sub>the</sub> <sub>different</sub> <sub>sheets</sub> <sub>in</sub> <sub>the</sub> <sub>Excel</sub> <sub>tool</sub> <sub>.</sub></p>
<p>In the following chapters, we will be exploring the different layouts and functions of each sheet.</p>
<h1 id="chapter-1.-data-table-sheet-layout">Chapter 1. Data Table Sheet Layout</h1>
<p>The KAP+ Excel Tool contains three data tables:</p>
<ul>
<li><strong>raw_data</strong> which contains strings (text) data,</li>
<li><strong>coded_data</strong> which codes the string data in <em>raw_data</em> into numeric data, and</li>
<li><strong>processed_data</strong> which groups the codes in the <em>coded_data</em> by variable and takes the variable scores.</li>
</ul>
<p>You can access the sheets either through clicking the links in the <em>Results</em> box in the <strong>intro</strong> sheet, or click the tabs found in the bottom part of the Excel interface. The <strong>summary sheets</strong> can be accessed in the same manner.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3cjgpiLHWY36vBlrSHHXkxLeq4-f-XtMqmEo83m1-WYg9X-MGPs-kwOwW-W2MDE9kH2nisMB4gi7Z6RI8mjATFDAp84qPAMc-VqFdZJB3FNZeEUcQYuGm8SFsgpSq3gv3vnqJKWtg-5oGagTfrXXsvN=w488-h47-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>6.</sub> <sub>Sheet</sub> <sub>tabs</sub> <sub>found</sub> <sub>in</sub> <sub>the</sub> <sub>bottom</sub> <sub>part</sub> <sub>of</sub> <sub>the</sub> <sub>Excel</sub> <sub>interface.</sub></p>
<p>The data table layout is divided into two parts: the <strong>indicator rows</strong> at the first three rows, and the <strong>observation rows</strong> which start from the fourth row and end depending on the sample size.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3fMUPaTgVpMlGtv6qkTM9705miSDvpUm0kY5AXDOTqVjCgwuEy0i_8U-BHKXtlQ-AQ2VDMsq3JDc2lXfTaVr0YEDoNBhqaYJzeg2c-nRgva4qJ4a2T_u8qVwV8EJrxguwpQLxffAkKOBMGPAPNEuFVO=w1705-h344-no?authuser=0" alt="data table layout "><br>
<sub>Fig.</sub> <sub>7.</sub> <sub>The</sub> <sub>data</sub> <sub>table</sub> <sub>layout.</sub> <sub>Indicator</sub> <sub>rows</sub> <sub>are</sub> <sub>in</sub> <sub>rows</sub> <sub>1</sub> <sub>to</sub> <sub>3</sub> <sub>while</sub> <sub>observation</sub> <sub>rows</sub> <sub>are</sub> <sub>in</sub> <sub>rows</sub> <sub>4</sub> <sub>and</sub> <sub>beyond.</sub></p>
<h2 id="indicator-rows">Indicator Rows</h2>
<p>The <strong>indicator rows</strong>  show the <strong>variable category row</strong> in row 1, <strong>variable row</strong> in row 2, and <strong>item row</strong> in row 3</p>
<p>The <strong>item row</strong> is also called the <strong>header row</strong> as it is usually used as the first row when data is exported into a .csv files</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3dqifEjhLGyb4o1dxiTgPj1U5DzG9-VwdB4UhFB3exw4ZFH3FQMrBsJmt8SDBFTuXgPIGBjKXuI2RtxVM17BvHndlU9auSRCyxFW9neAgaX2t2D5qc-gaoZJpG2xkaV89U_dlmTbrwBwXqtxDgNn_0w=w521-h90-no?authuser=0" alt="enter image description here"><br>
<sub>Fig.</sub> <sub>8.</sub> <sub>Indicator</sub> <sub>row.</sub> <sub>Row</sub> <sub>3</sub> <sub>is</sub> <sub>the</sub> <sub>header</sub> <sub>row.</sub></p>
<h3 id="a.-variable-category-row-row-1">A. Variable category row (Row 1)</h3>
<p>Variable category rows indicate which part of the survey a group of columns belong to.</p>
<p>The survey is divided into four or five main parts. Each part is uniformly color-coded in all iterations of the Excel tool for easy identification.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3dFOvYAeVyZtrLuXsclyyBOhGBf5wKI8pULitRMdrjk3--z04oLOSCi6-FW9-qcLGVIISMrCmU9h3XMac2J_YjCcBmOblqvmz9v9Ekt0F9MWLHfPEmebSlFnNRKAwF4uEpgYk3LQU09GMM3OM4wxI-X=w875-h335-no?authuser=0" alt="enter image description here"><br>
<sub>Fig.</sub> <sub>9.</sub> <sub>Color-</sub><sub>coding</sub> <sub>scheme</sub> <sub>for</sub> <sub>the</sub> <sub>survey</sub> <sub>parts.</sub> <sub>This</sub> <sub>color</sub> <sub>scheme</sub> <sub>is</sub> <sub>used</sub> <sub>consistently</sub> <sub>throughout</sub> <sub>the</sub> <sub>Excel</sub> <sub>tool.</sub><sup class="footnote-ref"><a href="#fn2" id="fnref2">2</a></sup></p>
<h3 id="b.-variable-row-row-2">B. Variable row (Row 2)</h3>
<p>Variable rows indicate what variables a group of columns belong to. As we will see later in this tutorial, variable scores are computed in the *<em>processed_data</em> sheet by summing up the columns that belong to specific variable rows.</p>
<p>For example, in this image below, items k1-k3 are attributes of the “Knowledge on Antibiotics” variable.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3eh6cmXjkEIdXJyekA-d9OSIAvG_4p7faVFQu1FtGsiLNFquvZecKQgfl_eNaJhyxv3JZwOuE4xCVUuehmHbJQgdecV3wxukY78C-7Qt0AGUgOmFeYdglMWsCuWn7JwrT8-9cGgCfZnUhCPQcbkDM2w=w311-h244-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>10.</sub> <sub>An</sub> <sub>example</sub> <sub>of</sub> <sub>a</sub> <sub>variable</sub> <sub>row,</sub> <sub>"Knowledge</sub> <sub>on</sub> <sub>antibiotics"</sub> <sub>in</sub> <sub>row</sub> <sub>2.</sub> <sub>The</sub> <sub>columns</sub> <sub>corresponding</sub> <sub>to</sub> <sub>the</sub> <sub>variable’</sub> <sub>cell</sub> <sub>are</sub> <sub>its</sub> <sub>attributes.</sub></p>
<h3 id="c.-itemheader-row-row-3">C. Item/Header Row (Row 3)</h3>
<p>Item rows indicate the individual items of the survey. Each item row cell follows the naming convention:</p>
<pre><code>#(surveypart|sd,k,a,p,s,i,c) + item no. + "_" + item description
</code></pre>
<p>for example:</p>
<blockquote>
<p>k1_ab<br>
(Knowledge item no. 1 on antibiotics)<br>
“Knowledge about antibiotics”</p>
</blockquote>
<p>Items which require <strong>multiple answers</strong> need to have a separate column per answer.</p>
<p>For example, take the following item which can have multiple answers:</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3cBH8q2hAd814v7s9wvHoa_1pHobCgAlKUgcmX6jFvhX-hU9nHSzIDf1ZTD2CXUOkopHES-Mieq_ZKcamopqFzfoIKSGLalzTO3ojny4xnuul4-nYoE7YE2RH5J2-Kio_cOdVIYS1-0aQq7Sph1slfL=w1367-h310-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>11.</sub> <sub>An</sub> <sub>example</sub> <sub>of</sub> <sub>an</sub> <sub>item</sub> <sub>which</sub> <sub>requires</sub> <sub>multiple</sub> <sub>answers.</sub></p>
<p>This item has to be spread in the Excel sheet into <strong>multiple columns</strong>, with each possible answer having one column. Items with mutiple columns are usually named like this:</p>
<pre><code>(Survey_part(sd,k,a,p,e,i,c) + item no. + lowercase letter + "_" + attribute
</code></pre>
<p>For example:</p>
<blockquote>
<p>SD12a_location_flatland, SD12b_location_sloping, SD13c_location_nearwater etc.</p>
</blockquote>
<p>These items are usually <strong>yes/no</strong> in nature (unless it calls for an <strong>open answer</strong>), and are usually inputted like so:</p>
<p>(<img src="https://lh3.googleusercontent.com/pw/ACtC-3cmHVWsp5sGlMU7m7pKyAiMG7FsiU_lzm9ZwhBf6XCAEaRxy3b1_QgNhKEPNng1XvUBVVcoqsZPF-T_MxEzLnMdFc2CxFHGtFbF_SnZi4lGwFnBI39kc3px18ArXtaga4Nz9df1G46U98QVDQ3G6SsF=w923-h634-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>12.</sub> <sub>An</sub> <sub>example</sub> <sub>of</sub> <sub>an</sub> <sub>item</sub> <sub>with</sub> <sub>multiple</sub> <sub>possible</sub> <sub>answers.</sub> <sub>Such</sub> <sub>items</sub> <sub>are</sub> <sub>spread</sub> <sub>into</sub> <sub>multiple</sub> <sub>columns</sub> <sub>with</sub> <sub>one</sub> <sub>column</sub> <sub>per</sub> <sub>possible</sub> <sub>answer.</sub></p>
<h3 id="common-abbreviations">Common Abbreviations</h3>
<p>For the sake of brevity, common abbreviations are used all throughout the Excel tools. These include:</p>

<table>
<thead>
<tr>
<th>abbreviation</th>
<th>meaning</th>
</tr>
</thead>
<tbody>
<tr>
<td>ab</td>
<td>antibiotic</td>
</tr>
<tr>
<td>abr</td>
<td>antibiotic resistance</td>
</tr>
<tr>
<td>abu</td>
<td>antibiotic use</td>
</tr>
<tr>
<td>am</td>
<td>antimicrobial</td>
</tr>
<tr>
<td>amr</td>
<td>antimicrobial resistance</td>
</tr>
<tr>
<td>amu</td>
<td>antimicrobial use</td>
</tr>
<tr>
<td>sd</td>
<td>socio-demographic</td>
</tr>
<tr>
<td>k</td>
<td>knowledge</td>
</tr>
<tr>
<td>a</td>
<td>attitude</td>
</tr>
<tr>
<td>p</td>
<td>practices</td>
</tr>
<tr>
<td>e</td>
<td>policy, information, and socio-cultural environment</td>
</tr>
<tr>
<td>i</td>
<td>interest</td>
</tr>
<tr>
<td>c</td>
<td>communication preferences</td>
</tr>
</tbody>
</table><h2 id="observation-rows">Observation rows</h2>
<p>Observation rows contain the answers of the survey respondents.</p>
<p>Each row from <strong>rows 4 to n</strong> is called an <strong>observation</strong>.  Observations are given a unique respondent ID number in the “ID” column in the leftmost part of the data table.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3eMDeFMrwBAGfn8cAw0Y3qz3nITV-eNw05n6Cty3ivQKRA7yCjxBn0XGIKepz8etCUiyv2lJdowwVcXdLky4CwFQ4z-5X_hL4_fNCi8-2fn5EaaW5eXK9kitPai4FjmTxtdWo3DZa7ZQTGDFrCHrr3r=w1628-h487-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>13.</sub> <sub>The</sub> <sub>observation</sub> <sub>rows;</sub> <sub>Observations</sub> <sub>start</sub> <sub>at</sub> <sub>row</sub> <sub>4</sub> <sub>and</sub> <sub>are</sub> <sub>assigned</sub> <sub>with</sub> <sub>a</sub> <sub>unique</sub> <sub>ID</sub> <sub>number.</sub></p>
<h1 id="chapter-2.-data-table-sheet-functions">Chapter 2. Data Table Sheet Functions</h1>
<p>The <em>data table sheets</em> contain different modes of the same data. This is useful especially when you plan to do a more robust analysis with a combination of raw, coded, and variable score data.</p>
<h2 id="raw_data">raw_data</h2>
<p>Before inputting any data in the <strong>raw_data</strong> sheet, you need to open the <em>codebook</em> in the <strong>intro</strong> sheet to see what specific words or phrases you have to input in a cell.</p>
<p>These inputs are shortened versions of the answers found in the <em>survey sheets</em>. For example, in the following survey question, the answer choices for <em>question 001</em> are too long to input in a single Excel cell.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3dSJdCdpLYp-HsvHCuYzmsxWjziyZx6gdvsDlPVS9Byc2_yzmQ8GoW4cGKctM4PUx7atXO3YUyliQyszR0Y10Afn38BLG0sBr_h0keWrb7E2DN9zfRqdRxO6krenSK80mLsxFvJFZjr9eoSexj-nO_F=w1351-h400-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>14.</sub> <sub>An</sub> <sub>item</sub> <sub>from</sub> <sub>the</sub> <sub>survey</sub> <sub>sheets.</sub> <sub>Answers</sub> <sub>are</sub> <sub>too</sub> <sub>long</sub> <sub>to</sub> <sub>input</sub> <sub>in</sub> <sub>a</sub> <sub>single</sub> <sub>Excel</sub> <sub>cell.</sub> <sub>Codes</sub> <sub>in</sub> <sub>the</sub> <sub>rightmost</sub> <sub>cell</sub> <sub>are</sub> <sub>automatically</sub> <sub>coded</sub> <sub>in</sub> <sub>coded_</sub><sub>data.</sub></p>
<p>If you refer to the <em>codebook</em> version, you will see that the same answer choices have been shortened (e.g. “Finished Post-Graduate Studies” has been shortend to “post-graduate”). The item number has also been modified into its corresponding <strong>item row</strong> format for easy referencing.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3dCCv2lM3TUWyR6Cu2tu9_eqgOyJELHDPg02S-Zp901uVgUPludjV1cwbslnncF0Y-yAgj8yy-4z1aNH8gkjnY4iLxPDCKqzSBDDxN3KedegSncIgLH39cQBvcBfniAwv8HQ6ZAWxo0yGgiT5371h_7=w1094-h283-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>15.</sub> <sub>The</sub> <sub>same</sub> <sub>item</sub> <sub>in</sub> <sub>Fig.</sub> <sub>11</sub> <sub>in</sub> <sub>the</sub> <sub>codebook.</sub> <sub>Its</sub> <sub>answer</sub> <sub>choices</sub> <sub>are</sub> <sub>shortened.</sub></p>
<p>Although the Excel tool is <em>case-insensitive</em>, we suggest that all cell inputs are written in <strong>lowercase</strong> for ease of reading and compatibility with different statistical software and/or programming languages.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3cxYBhF6OGbCdmLvZbKMYHr7LaHbCR1adNhye8H6jM8OpSj6_bejLCTYrh6YHnvQbNCw5kT4t1mxeZ47VUaOx87zbo7ML9PHsydDGa2ONC6lyhV0NDVXfajMtnKqWmIWJeKHIqBxDeZiCCr6Lng_1W-=w440-h269-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>16.</sub> <sub>Example</sub> <sub>raw_</sub><sub>data</sub> <sub>input</sub> <sub>in</sub> <sub>SD1_education.</sub></p>
<p>Some items require <strong>open answers</strong>. You can input any word or phrase in the cell and it will be coded as “1”, although we recommend to keep the input as short as possible. To indicate that the respondent has no answer or cannot remember, input “<strong>na</strong>”.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3eWCycqkADj_1NlR4VoPhywJj1e2o9M4aNzsxbwOR_oYsQnQoUTrXHa5r8ttcHLYIZnvU9Sy66zbiluyGpjUT_T-ZBT0JyAiFZCoQgN-J2QaevVw47mLL02j5dpceoa11jMRuvcKXZItzBkPS8t0hol=w1368-h189-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>17.</sub> <sub>An</sub> <sub>item</sub> <sub>requiring</sub> <sub>open</sub> <sub>answers.</sub> <sub>The</sub> <sub>Excel</sub> <sub>tool</sub> <sub>will</sub> <sub>code</sub> <sub>any</sub> <sub>answer</sub> <sub>as</sub> <sub>“1”</sub> <sub>except</sub> <sub>for</sub> <sub>"can’t</sub> <sub>remember</sub> <sub>"</sub> <sub>and</sub> <sub>"na</sub><sub>".</sub></p>
<h3 id="using-na-when-a-respondent-does-not-have-an-answer-or-when-a-respondent-is-not-applicable-to-answer-certain-items">Using “na” when a respondent does not have an answer, or when a respondent is not applicable to answer certain items</h3>
<p>To indicate that the respondent does not have an answer, please input “<strong>na</strong>”  (as “no answer”) in the corresponding cell so the tool codes the answer as “0”.</p>
<p>The <strong>“na”</strong> (as "not applicable) can also be used in case an item is not applicable for certain participants. For example, take the following item:</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3f2TCiUSsgUa1haslu9WhB4SMzxQKkuqlDMVzHVKDBw9hhOhmuaG_90RScYmNaIyEpl1qnlgrcCMsFuqBxMKTh_XrWje6KDMxamL15ry2wrpIjvMirRvUF7epSvlIDaoTGTBpGWiiRUx0ZFXCfoT-o2=w1360-h428-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>18.</sub> <sub>Item</sub> <sub>005</sub> <sub>is</sub> <sub>an</sub> <sub>example</sub> <sub>of</sub> <sub>an</sub> <sub>item</sub> <sub>that</sub> <sub>can</sub> <sub>only</sub> <sub>be</sub> <sub>answered</sub> <sub>depending</sub> <sub>on</sub> <sub>the</sub> <sub>participants</sub> <sub>previous</sub> <sub>answer/s.</sub></p>
<p>In the following arrays of data, respondents who answered “no” and “don’t know” in <em>item 004</em> (K4_am) are not applicable to answer question 5. So for observations with “no” or “na” in K4_am, you need to input “<strong>na</strong>” in <em>item 005</em> (K5_am_use) to indicate that the respondent in the said rows are not applicable to answer the latter item. The Excel tool recognizes this and codes “na” as “0”.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3ckB3R-7VmAnR3HOs_PTeZEqNJwidRzIrfYMQl_qszJYbiEb-B6jyuTTHV7sH4VleI3U1v2AnD-b0JgMJi4et8_7qX45FN2PwyBuYS_-Wpzu5Hymq4dzaNAsSQFIgVUHIe0E0Yq4qIDZSXstxVbl8wt=w784-h520-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>19.</sub> <sub>How</sub> <sub>to</sub> <sub>input</sub> <sub>"not</sub> <sub>applicable"</sub> <sub>items</sub> <sub>in</sub> <sub>raw_</sub><sub>data</sub> <sub>with</sub> <sub>“na”.</sub> <sub>Rows</sub> <sub>with</sub> <sub>“no”</sub>  <sub>and</sub> <sub>“na”</sub> <sub>answers</sub> <sub>in</sub> <sub>K4_am</sub> <sub>are</sub> <sub>not</sub> <sub>applicable</sub> <sub>to</sub> <sub>answer</sub> <sub>K5_am_use.</sub></p>
<h2 id="coded_data">coded_data</h2>
<p>The <strong>coded_data</strong> sheet codes the answers in <strong>raw_data</strong> based on the codes assigned to the answer choices in both <em>codebook</em> and <em>survey sheet</em>.</p>
<p>The sheet works by using different Excel functions that recognize input from <strong>raw_data</strong> and codes them based on the function’s coded instructions. For example, yes-no questions are usually coded with the function:</p>
<pre><code>=IF(raw_data!"Cell directory" = "yes", 1, 0)
</code></pre>
<p>This basically codes “yes” as “1” and anything else as “0”. This is also why you need to refer to the <em>codebook</em> when inputting data in the <strong>raw_data</strong> sheet as the tool might not recognize other inputs and thus produce the wrong code.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3en99-hc5V23alUA5CCZvOzlIty6VfkeczOvlC3DIw0xyDa76QuNlBB-ngnBrVQgjBNS4Lxjop8DyHZhbXx6_-b9PQaLtujLH2v2pz1Os5ZKWXwa4if0hTi2ixfWWltCi9G3u9gEiqXEUtxNJCeockX=w755-h427-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>20.</sub> <sub>Diagram</sub> <sub>showing</sub> <sub>how</sub> <sub>coded_data</sub> <sub>uses</sub> <sub>functions</sub> <sub>to</sub> <sub>code</sub> <sub>inputs</sub> <sub>from</sub> <sub>raw_data.</sub></p>
<h2 id="processed_data">processed_data</h2>
<p>As the <strong>coded_data</strong> sheet only codes individual items, there is a need to further process the coded data in order to get the variable scores. As seen earlier, variables in the tool are composed of a unique group of items.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3dgiLy784Etv5ikUxfbQ-_K5h7--Shmq8bX3MnMCnueG0zMCfRH1VMkTU7cwWTp4MWlRSf5Vv2GK8z5ngRLMpd64GMWPYZvNTrks_nW_1jiVA_88-5HPGf-dURJ49gGKChffX7V9OqsXCwQ2OTIpfu8=w312-h244-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>21.</sub> <sub>An</sub> <sub>example</sub> <sub>of</sub> <sub>a</sub> <sub>variable,</sub> <sub>"Knowledge</sub> <sub>on</sub> <sub>antibiotics</sub><sub>".</sub></p>
<p>The <strong>processed_data</strong> sheet does several computations to get the following variable scores:</p>
<ol>
<li>(raw) variable score</li>
<li>respondent’s percentage of correct answers</li>
<li>indices</li>
<li>index rankings</li>
</ol>
<p>The <strong>processed_data</strong> sheet takes the raw <strong>variable scores</strong> by adding the coded data values of the unique group of items that constitute a variable.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3fNL3QZDsGoj75V-Dn-FmUp_yt5cjnc3qZH0YmRa8EcNGDO0KloUQOD-IKVVWn_xZiH_Uv4qqPu7EBFJvZk8gs7y5aQOi_H3MTRdjLKEyX_dD2RfK7qK3hYbCzt7VkRAcUa_YPavDVy3oH639lpVZvL=w756-h427-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>22.</sub> <sub>Diagram</sub> <sub>showing</sub> <sub>how</sub> <sub>a</sub> <sub>variable</sub> <sub>score</sub> <sub>is</sub> <sub>computed.</sub></p>
<p>The variable scores, however, may not be applicable for analysis yet (depending if the user opts to go for parametric, non-parametric, or machine learning techniques). So the variable scores are further processed into three different answer types:</p>
<ol>
<li>Ratio of the each respondent’s variable score over the perfect variable score (expressed in percentage); and</li>
<li>The index of the ratio score in (1) and its corresponding ranking which is based on a quartile division of 100%:</li>
</ol>

<table>
<thead>
<tr>
<th>Index</th>
<th>Rank</th>
</tr>
</thead>
<tbody>
<tr>
<td>r &gt;= 80%</td>
<td>very high</td>
</tr>
<tr>
<td>r &gt;= 60%</td>
<td>high</td>
</tr>
<tr>
<td>r &gt;=40%</td>
<td>moderate</td>
</tr>
<tr>
<td>r &gt;= 20%</td>
<td>low</td>
</tr>
<tr>
<td>r &gt;= 0%</td>
<td>very low</td>
</tr>
</tbody>
</table><p><img src="https://lh3.googleusercontent.com/pw/ACtC-3cRmKHR5SmVNQQmbKUQmTMZeXEiAzLDIlXUR7YQJS2yHgFkQspFuP_23D2r9A5hWheAAfPSfkB9YUYqIbGmiM4sjxBl82cIfgTx7idTlxHMiYok0cNMXt6fORkYNmgWRnN8V9OvqqGwPBx8qC21UAkJ=w836-h427-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>23.</sub> <sub>Diagram</sub> <sub>showing</sub> <sub>how</sub> <sub>variable</sub> <sub>scores</sub> <sub>are</sub> <sub>further</sub> <sub>processed</sub> <sub>into</sub> <sub>ratios,</sub> <sub>indices,</sub> <sub>and</sub> <sub>rankings.</sub></p>
<h1 id="chapter-3.-summary-sheets-layout-and-function">Chapter 3. Summary Sheets Layout and Function</h1>
<p>The summary sheets summarizations of the data tables and exploratory analyses. These sheets are automatically updated after updating the <strong>coded_data</strong> and <strong>processed_data</strong> sheets.</p>
<p>Moreover, the summary sheets cannot be imported into other statistical software</p>
<h2 id="survey_answers">survey_answers</h2>
<p>The <strong>survey_answers</strong> sheet contain all the questions in the <em>survey sheets</em> and show the sample score, percentage of correct answers, indices, and rankings per item.</p>
<p>Each survey part has its own <em>table/s</em>. You can sort the values in the table by clicking the header buttons. This allows you to sort scores from highest to lowest and vice-versa.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3ecLiRxejcYpIFehimq-DbaB4pfbSpP8TqOZy8DmwOsdh-stQplnhz_HfCKYTQC2XckbvfC6LE6xJSHFG-SRsKWwOSq-beWFRkbMQrPLFE7KwrvUMQ4k0XhEzbWmHFpB3gIJkS_hAxkSzj1QsGHhR9K=w1200-h606-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>24.</sub> <sub>Example</sub> <sub>of</sub> <sub>a</sub> <sub>table</sub> <sub>in</sub> <sub>the</sub> <sub>survey_</sub><sub>answers</sub> <sub>sheet.</sub> <sub>The</sub> <sub>GIF</sub> <sub>above</sub> <sub>shows</sub> <sub>how</sub> <sub>to</sub> <sub>sort</sub> <sub>values.</sub></p>
<h2 id="summary">summary</h2>
<p>The <strong>summary</strong> sheet calculates measures for <em>central tendency</em> and <em>spread</em> for each variable in the <strong>processed_data</strong> sheet.</p>
<p>It also calculates the raw sample score, percentage of correct scores, indices, and index ranking for each variable.</p>
<p>Variables are grouped into tables based on which part of the survey they belong to. The same color coding shown in Chapter 1 applies in the sheet.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3ecfM15rU6bYefvmzQstmGPinyPT9wS6xHHBEtsrWZYUhZDX9VptdfJq0l5Mtc0uwKHqIBhVvzk6NFvOXisWAOsSqgXV_DOc6ptMslK96MBtQr68FrK6djhpMqcVOYphmbc0HZDL-Uf3hg6puyP5vnt=w1787-h596-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>25.</sub> <sub>An</sub> <sub>example</sub> <sub>of</sub> <sub>the</sub> <sub>summary</sub> <sub>sheet</sub></p>
<h2 id="correlation">correlation</h2>
<p>The <strong>correlation</strong> sheet measures significant correlations of variables from the <strong>processed_data</strong>. The tool uses the raw scores from the <em>_score</em> columns in calculating for the Pearson coefficient.</p>
<p>Correlation in Excel is tricky because it requires extra steps in order to get the p-values and determine if a correlation is significant.</p>
<p>To do this, we need to get the <strong>t-value</strong>  of the <strong>correlation coefficient</strong> to get its <strong>p-value</strong>. The following diagram shows how we can do it in Excel.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3e5kYq3lN6r4jLWRw3lUB2yUErOPcHzmHJD3oV2qpCQRmdWHoMI9mSACO_8UfNJ6Zk3Ham9NWS1rzCn-beweSa1QGh0qzAASYpViRlwTL9wBjGdVNLI5RkgPFXbVmwKtLuaWUDdbH9mnPYTcV0Dk_U2=w651-h641-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>26.</sub> <sub>Diagram</sub> <sub>showing</sub> <sub>how</sub> <sub>to</sub> <sub>calculate</sub> <sub>the</sub> <sub>Pearson</sub> <sub>coefficients,</sub> <sub>t-values,</sub> <sub>and</sub> <sub>p-values</sub> <sub>in</sub> <sub>the</sub> <sub>Excel</sub> <sub>tool.</sub></p>
<p>Fortunately, the Excel tool automatically computes the correlation coefficient, its t-value, and its p-value, and also flags if the p-value is significant at p &lt; 0.05 and p &lt; 0.01.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3ebk14CxaOu-jX52vlwNJ_Qo10rscUUDOQ9grJWIf6EQq7_B2fbM1tkxvpTmrRkVhU7I3Q29E7ZCEa9tXL3rIOEosbbzKE9M85qW7IRSQe4ZzrlwtTzMpFLTHJEJ2RRF6X-nrs4TIqyX_xeV9cY4krU=w1230-h231-no?authuser=0" alt=""><br>
<img src="https://lh3.googleusercontent.com/pw/ACtC-3fF9MNdBKLytJa-eLHKp5zzeMuyPw14ESsW-pcj1wxnwpsmgJ53Pnq7XCFMvawUSRRWeIoKixdip2xf_pBOMqT1dDzdmeT7d8rIVwxqf1UKZohTK5w2pPLkUox0su5inUa8l_0EW_7Jcsg3i4bNsEa_=w1230-h231-no?authuser=0" alt=""><br>
<img src="https://lh3.googleusercontent.com/pw/ACtC-3ecUB93QvCsUY3L9Eyd0R__czVEdJXS5pc-hZOgB5siZCNSGu-IgTcMJ1CwGftzCYy4XWdKTzFBWdNK7-XNTysD_nTp2pnbQXtzLnuE84LgPuvf6tcVnpE8aeRLs2wsIFN4j5JVFzNnuZU6EkqSZBOD=w1235-h225-no?authuser=0" alt=""><br>
<sub>Figs.</sub> <sub>27-29.</sub> <sub>Example</sub> <sub>of</sub> <sub>correlation</sub> <sub>tables</sub> <sub>in</sub> <sub>the</sub> <sub>Excel</sub> <sub>tool.</sub> <sub>The</sub> <sub>p-values</sub> <sub>are</sub> <sub>flagged</sub> <sub>with</sub> <sub>color</sub> <sub>highlights</sub> <sub>when</sub> <sub>found</sub> <sub>to</sub> <sub>be</sub> <sub>significant</sub> <sub>at</sub> <sub>p</sub> <sub>&lt;</sub> <sub>0.05</sub> <sub>or</sub> <sub>p</sub> <sub>&lt;</sub> <sub>0.01.</sub></p>
<h1 id="chapter-4.-adding-and-updating-the-data-sheets">Chapter 4. Adding and Updating the data sheets</h1>
<h2 id="adding-data-to-raw_data">Adding data to raw_data</h2>
<p>To input new observations of survey answers in the <strong>raw_data</strong> sheet:</p>
<ol>
<li>Add the corresponding ID number of new observations in the first column,</li>
<li>To input answers, refer to the <strong>codebook</strong> for the specific words and phrases that are recognized by the tool. These words and phrases are mostly shortened versions of the answers in the <strong>survey sheets</strong></li>
</ol>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3cpnmroz6Xa54zN5WWiiV6zl4zjXmQbAve8sL-yB3H0SXt_4aWfuQtv8m07mPfO18bxqiJAUVQfKc6F1KVAL_D0Dig-Bh8YfaFEHe-GMwwuEyukBGW8MGC5FWRLZPwl00YYDmzgidz0WRIv1RJJqKAt=w1030-h472-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>30.</sub> <sub>Inputting</sub> <sub>new</sub> <sub>observations</sub> <sub>(shown</sub> <sub>in</sub> <sub>red</sub> <sub>text).</sub></p>
<h2 id="updating-coded_data-and-processed_data">Updating coded_data and processed_data</h2>
<p>Updating the <strong>coded_data</strong> and <strong>processed_data</strong> sheets only requires you to drag the functions in previous cells down to the row number of your inputted data. So if you added data from rows 14 to 16 in <strong>raw_data</strong>, simply drag and drop the functions from row 14 down to 16 in both <strong>coded_data</strong> and <strong>processed_data</strong>. For example:</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3d3shYdmFWI9xHP8ydumVF6YOwAdWQREULaj_GCf49nt-V-y4M3HzjkhaUzu7Kc6KVpp0XFGbGK62kJ6zHSVBl9F1wTH77dAfoS-bIy2QHOWWWHp-Gsv2WwScroOZs7iD3ebQvMgUN6x6EKVlSFMAoW=w1034-h462-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>31.</sub> <sub>Updating</sub> <sub>the</sub> <sub>coded_data</sub> <sub>and</sub> <sub>processed_data</sub> <sub>sheets</sub> <sub>through</sub> <sub>Excel’s</sub> <sub>drag-and-drop</sub> <sub>function</sub> <sub>(new</sub> <sub>observations</sub> <sub>shown</sub> <sub>in</sub> <sub>red</sub> <sub>text).</sub></p>
<p>The <strong>summary sheets</strong> update on their own as the <strong>indicator sheets</strong> need to be manually updated.</p>
<hr>
<h1 id="chapter-5.-exporting-to-.csv">Chapter 5. “Exporting” to .csv</h1>
<p>Since the Excel tool can only handle a limited number of analyses, running more robust statistical analyses will require the user to import data from the Excel tool into a .csv file.</p>
<p>The easiest way to do this is to <em>manually copy</em> the data you need from the data tables starting from row 3 (item number in <strong>raw_data</strong> and <strong>coded_data</strong>, and variable name in <strong>processed_data</strong>) down to the last row of observations, and paste them in a <strong>new</strong> Excel file.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3eqj156dHgoQB45LqQo7kcPT22yG4v0PZ1YcSSaAXTaiD__Mm-kEz_xDscDEIeGyFZpuekPdpFmdXBCUhwQCtY4E5JrZxY9YmDK3dxsZbAW_wHzd3q1--ReJXNPQi-RemtakQxGxPN-UNOOJAdHHzhE=w1789-h527-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>32.</sub> <sub>Selecting</sub> <sub>the</sub> <sub>data</sub> <sub>to</sub> <sub>be</sub> <sub>copied</sub> <sub>into</sub> <sub>a</sub> <sub>new</sub> <sub>Excel</sub> <sub>file</sub> <sub>to</sub> <sub>be</sub> <sub>exported</sub> <sub>into</sub> <sub>.csv</sub> <sub>format.</sub> <sub>Row</sub> <sub>3</sub> <sub>is</sub> <sub>used</sub> <sub>as</sub> <sub>the</sub> <sub>data</sub> <sub>frame</sub> <sub>header.</sub></p>
<p>The new Excel file can be saved in .csv format.</p>
<p><img src="https://lh3.googleusercontent.com/pw/ACtC-3fi9ryVn1VHEtS7hf94rZcCSo0GmWmcMgRDDG-SQZZ0ts5nAjFbhGVPWTDG576w_5eqv1la_HJ4SZ6h2gmq91CJg7WMJA92vvCs12RP-xuYcQKB_H1enbIUxh0-EHobhWgj5cHqr8eFHFk9pb5P3Pa7=w1289-h703-no?authuser=0" alt=""><br>
<sub>Fig.</sub> <sub>33.</sub> <sub>A</sub> <sub>new</sub> <sub>Excel</sub> <sub>file</sub> <sub>with</sub> <sub>the</sub> <sub>data</sub> <sub>to</sub> <sub>be</sub> <sub>exported</sub> <sub>into</sub> <sub>.csv</sub> <sub>format.</sub></p>
<hr class="footnotes-sep">
<section class="footnotes">
<ol class="footnotes-list">
<li id="fn1" class="footnote-item"><p>A mini-tutorial featuring a sample data manipulation and analysis in R can be found in the <em>demo</em> folder of the GitHub repository. <a href="#fnref1" class="footnote-backref">↩︎</a></p>
</li>
<li id="fn2" class="footnote-item"><p>Slight variations in hue may be used. <a href="#fnref2" class="footnote-backref">↩︎</a></p>
</li>
</ol>
</section>

    </div>
  </div>
</body>

</html>