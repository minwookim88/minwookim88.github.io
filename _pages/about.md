---
permalink: /about/
title: ""
---
<h1 id="bio">Bio</h1>
<div>
<p>
My name is Minwoo Kim, and I am a data scientist and software engineer.
I studied <b>Mathematics</b> at <a href="https://en.wikipedia.org/wiki/KAIST" target="_blank"><b>KAIST</b></a> (Korea Advance Institute of Science and Technology) for BS, majored in <b>Statistics</b> at <a href="https://en.wikipedia.org/wiki/Seoul_National_University" target="_blank"><b>Seoul National University</b></a> for MS, and hold another MS in <b>Computer Science</b> at <a href="https://en.wikipedia.org/wiki/Duke_University" target="_blank"><b>Duke University</b></a>.
</p>

<p>As for the specific area I was exposed to, I studied Real/Complex Analysis, Linear algebra, Abstract Algebra, Measure Theory, Probability Theory, Topology, Differential Geometry, Regression Analysis, Non-parametric Regression, Density Estimation, Markov Chain, Statistical Inference, Statistical Theory, Kernel Smoothing, Algorithm, Database, Signal Processing, Markov Decision Process, and Parallel Computing.
</p>



<p>
I am currently living in
<i class="fa fa-map-marker-alt"></i>
<a href="https://www.google.com/maps/place/Santa+Clara,+CA/@37.3709535,-122.002572,13z/data=!3m1!4b1!4m5!3m4!1s0x808fb7815c08c193:0xe475a47ca3c0bfc0!8m2!3d37.3541079!4d-121.9552356" target="_blank">Santa Clara, CA</a>.
</p>
</div>

<h1 id="projects">Projects</h1>
<!---  
====================================================================================================
--->
<h4>
<i class="fa fa-tasks" aria-hidden="true"></i>
Detect Malfunction of LTE Tower
<button type="button" class="collapsible" id="coll1_button" style="float:right;">Details
<i class="fa fa-arrow-down" aria-hidden="true"></i>
</button>
</h4>

<div>
Detected precursory symptoms of malfunction by monitoring behaviors of RBS's (Radio Base Station) PM (Performance Measurement) counters.
</div>

<div class="content" id="coll1">
<ul>
<li>
Built a robust timeseries model that learns normal behavior (=baseline of timeseries data) of multivariate PM  counters based on quantile regression, so that the model is robust to anomalous activities.
</li>
<li>
Built a graphical model that learns data-driven hierarchical structure among PM counters (#=~700). This helped in understanding dependence structure between PM counters, revealing functional subsystems which enables the detector to further identify the source of malfunction.
</li>

<li>
Built a visualization web-app that automatically provides the results of analysis per query basis. Used PostgreSQL for data hosting, JavaScript/D3.js for front-end and Flask/Python for back-end.
</li>

<li>
Built a python REST API that allows users to query and fetch the analysis results from the server on the fly. Used Connexion, Flask with OpenAPI specifications. Used Ray for parallelization.
</li>

<li>
Built a clustering model that identifies behavioral cohorts of RBS' with respect to PM patterns. This helped in understanding possible collective malfunctions occuring in the same region. Used CUDA kernel (Numba) to expedite the computation of large matrices.
</li>

<li>
Built a demo of automatic detection software that allows users to monitor and analyze behaviors of PM counters in real-time. 
</li>
<div>
<figure>
<img src="/assets/images/about/demo_snapshot_blurred.png">
<figcaption>Snapshot of Demo (blurred on purpose)</figcaption>
</figure>
</div>

<!---
<li>
classified fault types based on the geo-spatial co-occurrence patterns using
graphical models.
</li>
--->
</ul>
</div>


<!---  
====================================================================================================
--->
<h4>
<i class="fa fa-tasks" aria-hidden="true"></i>
Detect Fradulent Doctors
<button type="button" class="collapsible" id="coll2_button" style="float:right;">Details
<i class="fa fa-arrow-down" aria-hidden="true"></i>
</button>
</h4>

<div>
Detected fradulent medical prescription records from prescription data using link analysis.
</div>

<div class="content" id="coll2">
<ul>
<li>Built graphical models that capture interactions between different types of entities in the data - <b>doctor, pharmacy, patient, and drug</b>.
</li>
<li>Used <a href="https://en.wikipedia.org/wiki/PageRank#Internet_use" target="_blank">Personalized PageRank</a> to model the <b>flow of patient visits</b> within the provider (doctors and pharmacies) network. Then, any provider represented by sink or isolated nodes are considered as
ultimate points and assigned high anomaly scores accordingly.
</li>
<li>
Ran <a href="https://en.wikipedia.org/wiki/SimRank" target="_blank">SimRank</a> to quantify the similarity in medical activities between entities, and assigned high anomaly scores to any entities that turned out to be unusual in terms of the computed similarities.
<ol>
<li>Between <b>drugs</b> and <b>doctors</b>: <br>
The model assigned high similarity scores between doctors if the types of drugs they prescribed are similar. Then, the similarity scores were compared to their specialties and high anomaly scores were assigned to doctors who were unusual.
</li>
<li>Between <b>patients</b> and <b>pharmacies</b>: <br>
The model assigned high similarity scores between patients if they frequented to the same pharmacy.
Then, the similarity scores were compared to pharmacies' geo-locational similarities (=geographical distances).
</li>
<li>Between <b>patients</b> and <b>doctors</b>: <br>
The model assigned high similarity scores between patients if they frequented to the same doctor.
Then, the similarity scores were compared to doctors' geo-locational similarities (=geographical distances).
</li>
<li>Between <b>patients</b> and <b>drugs</b>: <br>
The model assigned high similarity scores between patients if they were prescribed the same types of drugs. Those who were too different (either they were prescribed the same drugs repeatedly or they were frequently prescribed the drugs that were not common in general) from other patients in terms of drug use were assigned high anomaly scores.
</li>
</ol>
<li>
Combined all the results from the above $1+4$ models to give the final anomaly scores for each entity.
Then, ranked the anomalous patients, doctors, and pharmacies accordingly.
</li>
</li>
<!---
<li>Reported suscipicious activities to medical insurance company so that they can focus on the suggested cases and further investigate them: this greatly reduced the cost for the duty of on-site investigation.
</li>
--->
</ul>

<div>
    <div style="width:50%;float:left;">
        <figure>
	  <img src="/assets/images/about/alldocs.png"
           style="width:100%; height:200px;">
          <figcaption>All Doctors' Locations</figcaption>
        </figure>
    </div>
    <div style="width:50%;float:left;">
        <figure>
	  <img src="/assets/images/about/frauddocs.png"
          style="width:100%; height:200px;">
          <figcaption>Anomalous Doctors' Locations</figcaption>
        </figure>
    </div>
</div>

</div>
<!---  
====================================================================================================
--->
<h4>
<i class="fa fa-tasks" aria-hidden="true"></i>
Analyze Hot Issues on Twitter
<button type="button" class="collapsible" id="coll3_button" style="float:right;">Details
<i class="fa fa-arrow-down" aria-hidden="true"></i>
</button>
</h4>

<div>
Built a wordcloud app that visualizes the current hot issues in real time.
</div>

<div class="content" id="coll3">
<ul>
<li>
Crawled the tweets through API, while parallerizing the task using <b>MPI</b> (Message Passing Interface) due to massive amount of data.
</li>
<li>
Used a <b>HMM</b> (Hidden Markov Model) to detect keywords in a given sentence; Trained the required parameters (off-line) first using corpus data
from <a href="https://www.nltk.org/" target="_blank">NLTK Library</a> in Python,
then, viterbi algorithm is implemented (in C++ for enhanced performance) to generate keywords from a huge volume of streaming tweets (on-line).
</li>
<li>
Visualized the summary of the analysis for every $10$ mins using <b>wordcloud</b> format.
</li>
</ul>

<div>
<figure>
    <div style="width:50%;float:left;">
	<img src="/assets/images/about/NYT.png"
         style="width:100%; height:200px;">
    </div>
    <div style="width:50%;float:left;">
	<img src="/assets/images/about/BBC.png"
         style="width:100%; height:200px;">
    </div>
    <div style="width:50%;float:left;">
	<img src="/assets/images/about/wapost.png"
         style="width:100%; height:200px;">
    </div>
    <div style="width:50%;float:left;">
	<img src="/assets/images/about/WSJ.png"
         style="width:100%; height:200px;">
    </div>
<figcaption>Snapshot of the analysis</figcaption>
</figure>
</div>
</div>
&nbsp;

<h1 id="trivia">Trivia</h1>
<p>
I like music, especailly listening, but also do have interests in
composing and playing myself; I had played the piano for 7 years, and played mostly classic music from Mozart, Beethoven, Bach, and Chopin (not currently though, unfortunately).
The last piece I played was <a href="https://www.youtube.com/watch?v=75x6DncZDgI" target="_blank">Fantaisie Impromptu, Op. 66</a> by Chopin,
which was the reason why I 
</p>




