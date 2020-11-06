<h4>Reproducing Faceforensics++: Learning to detect manipulated facial images (<a href="https://github.com/ondyari/FaceForensics">Github</a> <a href="https://arxiv.org/abs/1901.08971">Source Paper</a> )</h4>

<p>To reproduce the same results, the dataset need to be downloading using this <a href="https://docs.google.com/forms/d/e/1FAIpQLSdRRR3L5zAv6tQ_CKxmK4W96tAab_pfBu2EKAgQbeDVhmXagg/viewform">form</a> by agreeing to their terms & conditions.</p>
<p>Repository Descprition:<br>
This repostitory is a major project ,part of the course unit <b>COMP8240 - Applications of Data Science</b>
</p>
<h5>Team Members (Group H):</h5>
<ol>
	<li>Sai Diwakar Bhrugubanda (45852189)</li>
	<li>Saiprudhvi Meda ()</li>
	<li>Rahul Sonkusare</li>
	<li>Shruti Tyagi</li>
</ol>
<hr>
<h4>Stages of Implementation:</h4>
<p>There are two main stages of implemenation</p>
<ol>
	<li>Replication of original work</li>
	<li>Creating new data & applying on the original work</li>
</ol>


<h5>Replication of Original Work</h5>
<ul>
	<li>Data Extraction</li>
	<li>Data Pre-Processing</li>
	<p>File: <b>Original Work/ Data Pre-Processing.ipynb</b></p>
	<ul>
		<li>First faces are extracted from video frames using bounding boxes.</li>
		<li>Splitting the data and creating Train,Test and CV data.</li>
		<li>Shuffling the data and assigning class labels to every image 1 or 0 (Fake =1 and Real =0).</li>
		<li>Pickling the data to create .pkl files.</li>
	</ul>
	<li>Xception Modelling</li>
	<p>File: <b>Original Work/ Xceptionnet_Modelling.ipynb</b></p>
	<ul>
		<li>Import the pre-processed data i.e. Pickle files.</li>
		<li>Feed it into the model to pre-train and then test the accuracies using 2 variation of epochs.</li>
		<li>Evaluate the model on Train,CV and Test data to find accuracy of the model.</li>
	</ul>
	
</ul>
<h5>Creating new data & applying on the original work</h5>

<ul>
	<li>Creating New Data</li>
	<ol>
		<li>First Order Motion for images animation (Deep fakes)</li>
		<li>Acquired faceswap and face2face from thirdparty sources i.e youtube</li>
	</ol>
	<li>Xception Modelling</li>
</ul>

<h5>Citations:</h5>

<ol>
	<li>Rössler, Andreas & Cozzolino, Davide & Verdoliva, Luisa & Riess, Christian & Thies, Justus & Nießner, Matthias. (2019). FaceForensics++: Learning to Detect Manipulated Facial Images.</li>
	<li>Siarohin, Aliaksandr & Lathuilière, Stéphane & Tulyakov, Sergey & Ricci, Elisa & Sebe, Nicu. (2020). First Order Motion Model for Image Animation.</li>
</ol>

