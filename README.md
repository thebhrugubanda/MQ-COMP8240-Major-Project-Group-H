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
	<ul>
		<li>Using the script to download</li>
			<code>python download-Faceforensics.py <output path> -d all -c c23 -t videos</code>
		<li>Using the script to extract frames from the videos downloaded.</li>
			<code>python extracted_compressed_videos.py <output path> -d <"all" or single dataset via "Face2Face" or "original"> -c c23</code>
	</ul>
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
	<p> After using this <a href="https://docs.google.com/forms/d/e/1FAIpQLSdRRR3L5zAv6tQ_CKxmK4W96tAab_pfBu2EKAgQbeDVhmXagg/viewform">form</a>, we acquired script, and used the following commands to use these scripts</p>
	<ol>
		<li>First Order Motion for images animation (Deep fakes)</li>
		<p>File: <b>New Data/Creating-Deepfakes.ipynb</b></p>
		<p>Since the model is performing too well and creating perfect deepfakes, to test the XceptionNet model accuracy we are creating two types of deepfake videos.</p>
     	<ol>
     		<li>Deepfakes based on front facing images which create perfect deepfakes.</li>
     		<li>Deepfakes based on side angle images which create deepfakes that are little easy to differentiate between fake and real.</li>
     	</ol>
		<li>Acquired faceswap and face2face from thirdparty sources i.e youtube</li>
	</ol>
	<li>Xception Modelling</li>
	<p>File: <b>New Data/ Xceptionnet_Modelling(Front Facing Data).ipynb</b></p>
	<p>File: <b>New Data/ Xceptionnet_Modelling(Side Facing Data).ipynb</b></p>
	<p>Application of XceptionNet of 2 Variations of data i.e Front-Facing and 2. Side-Facing images</p>
</ul>

<h5>Citations:</h5>

<ol>
	<li>Rössler, Andreas & Cozzolino, Davide & Verdoliva, Luisa & Riess, Christian & Thies, Justus & Nießner, Matthias. (2019). FaceForensics++: Learning to Detect Manipulated Facial Images.</li>
	<li>Siarohin, Aliaksandr & Lathuilière, Stéphane & Tulyakov, Sergey & Ricci, Elisa & Sebe, Nicu. (2020). First Order Motion Model for Image Animation.</li>
</ol>

