# 99_Challenge
Technical Challenge 99 Data • New York City taxicabs • Isis Santos Costa, 2020

## Link to Notebooks, ordered per the data prep flow

<ol>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__DataExtraction.ipynb">Data Extraction</a></li>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__DataTransformation.ipynb">Data Transformation</a></li>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__DataTransformation2.ipynb">Data Transformation, part 2</a></li>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__DataTransformation3.ipynb">Data Transformation, part 2 (addendum)</a></li>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__DataTransformation3F.ipynb">Data Transformation, part 3 (soon!)</a></li>
  <!-- <li><a href="#Notebook_01">EDA</a></li> -->
 </ol>

<h2> Notebooks contents </h2>

<p id="#Notebook_01"><b> Notebook 1: DATA EXTRACTION </b></p>
<ul>
  <li> Connecting to DB </li>
  <li> From DB into DF </li>
  <li> DF into CSV </li>
  <li> Nᴇxᴛ: Transformation </li>
</ul>
</p>

<p id="#Notebook_02"><b> Notebook 2: DATA TRANSFORMATION </b></p>
<ul>
  <li> Setting the DataFrames
    <ul>
      <li> Taking a first look </li>
      <li> Naming the columns </li>
      <li> Basic inter-table consistency </li>
    </ul>
  </li>
  <li> Checking & improving the data structure
    <ul>
      <li> Trips x Orders </li>
      <li> Payment type </li>
      <li> Rate type </li>
    </ul>
  </li>
  <li> Exporting results for retrieval </li>
  <li> Continues as Transformation, part 2 </li>
</ul>
</p>

<p id="#Notebook_03"><b> Notebook 3: DATA TRANSFORMATION, part 2 </b></p>
<ul>
  <li> Resuming: retrieving the DFs </li>
  <li> Checking & improving the data structure (cont'd) </li>
    <ul>
      <li> Rate type (cont'd.) </li>
    </ul>
  <li> Basic information </li>
  <li> Converting strings into datetime </li>
  <li> Feature engineering: datetime 📅 </li>
    <ul>
      <li> Orders </li>
      <li> Trips </li>
    </ul>
  <li> Treating missing data </li>
  <li> Exporting results for retrieval </li>
  <li> Continues as: Transformation, part 3 (Final!) (lat, long) ➔ neighborhoods </li>
</ul>
</p>

<p id="#Notebook_04"><b> Notebook 4: DATA TRANSFORMATION, part 2 (addendum) </b>
<ul>
  <li> Resuming: retrieving the DFs </li>
  <li> Feature engineering: datetime 📅 (cont'd) [ Adding further new features for better analysis ]
    <ul>
      <li> 📈 Adding further new features for better analysis </li>
      <li> Orders </li>
        <ul>
          <li> Month </li>
          <li> Week in the month </li>
        </ul>
      <li> Trips </li>
        <ul>
          <li> Month </li>
          <li> Week in the month </li>
        </ul>
    </ul>
    </li>
  <li> Exporting results for retrieval </li>
  <li> Nᴇxᴛ: EDA </li>
</ul>
</p>

<p id="#Notebook_05"><b> Notebook 5: DATA TRANSFORMATION, part 3 </b>
<ul>
  <li> Resuming: retrieving the DFs </li>
  <li> Creating the features 'coordinates'</li>
  <li> Feature engineering: 📍coordinates into 🗺️neighborhoods (reverse geocoding) </li>
    <ul>
      <li> Preparing for heavy processing: autotime + tqdm (progress bar) </li>
      <li> Importing: Geopandas • Geopy (Nominatim+RateLimiter) • PyPlot • Plotly_express • TQDM </li>
      <li> Constructing Geocoder </li>
      <li> Reverse geocoding </li>
    </ul>
  <li> Exporting results for retrieval </li>
  <li> Nᴇxᴛ: EDA </li>
</ul>
</p>
