# 99_Challenge
Technical Challenge 99 Data • New York City taxicabs • Isis Santos Costa, 2020

## Link to Notebooks, ordered per the data prep flow

<ol>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__DataExtraction.ipynb">Data Extraction</a></li>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__DataTransformation.ipynb">Data Transformation</a></li>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__DataTransformation2.ipynb">Data Transformation, part 2</a></li>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__DataTransformation3.ipynb">Data Transformation, part 2 (addendum)</a></li>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__DataTransformation3F.ipynb">Data Transformation, part 3</a></li>
  <li><a href="https://github.com/IsisSantosCosta/99_Challenge/blob/main/99__EDA.ipynb">EDA (soon!)</a></li>
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
  <li> Continues as Data Transformation, part 2 (addendum) </li>
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
  <li> Continues as Transformation, part 3 (Final!) (lat, long) ➔ neighborhoods </li>
</ul>
</p>

<p id="#Notebook_05"><b> Notebook 5: DATA TRANSFORMATION, part 3 </b>
<ul>
  <li> Resuming: retrieving the DFs </li>
  <li> Combining the tables: outer join 🔗
    <ul>
      <li> Listing information added when orders get converted: trips_features </li>
      <li> Adding trips_features to the table of all orders </li>
      <li> 🗃️ Reordering the columns of the new DF df_orders_tF (𝘵ransformed, 𝘍inal) </li>
    </ul></li>
  <li> Feature engineering: 📍coordinates into 🗺️neighborhoods (reverse geocoding)
    <ul>
      <li> Preparing for heavy processing:
        <ul>
          <li> Exporting the dataframe as transformed so far 📤 </li>
          <li> Autotime + tqdm (progress bar) </li>
      </ul></li>
      <li> Importing: Geopandas • Geopy (Nominatim+RateLimiter) • PyPlot • Plotly_express </li>
      <li> Constructing Geocoder </li>
      <li> Reverse geocoding 
        <ul>
          <li> Pilot test ✔️ </li>
          <li> Full scale 📈, with Nominatim:
            <ul>
              <li> 1<sup>st</sup> trial, by list ❌ </li>
              <li> n<sup>th</sup> trial, by list ❌ </li>
              <li> ( Resuming after Kernel shut down • Retrieving data: nice it'd been saved! 😅 ) </li>
              <li> [ try / except ] ❌ </li>
              <li> [ try / except ] querying item by item ✔️ (kinda... 90 days!) </li>
              <li> [ numba / njit / numpy vectorize ] ✔️ (kinda: not fast enough) </li>
          </ul></li>
          <li> Full scale 📈, taking Einstein's advice:
            <ul>
              <li> « <i>As simple as possible</i>... </li>
              <li> ... <i>but not simpler</i> » </li>
              <li> Geometrical approach: using points and polynoms to define each borough </li>
              <li> Getting boroughs coordinates from Google Maps </li>
              <li> Defining a function for a « good enough » location of neighborhood </li>
              <li> Reverse Geocoding: the light way ✔️✔️✔️ </li>
              <li> Getting coordinates of Manhattan regions from Google Maps </li>
              <li> Defining a « good enough » function to locate Manhattan regions </li>
              <li> (Further) Reverse Geocoding: Manhattan regions ✔️✔️✔️ </li>
          </ul></li>
    </ul></li>
  </ul></li>
 <li> Lessons learned </li>
 <li> Preparing for the future: Creating aggregated data tables
   <ul>
     <li> Daily data </li>
     <li> Data by passenger </li>
   </ul></li>
  <li> Exporting results for retrieval </li>
  <li> Nᴇxᴛ: EDA </li>
</ul></li>
</ul>
</p>
