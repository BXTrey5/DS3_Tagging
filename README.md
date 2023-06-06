# Automated Tagging of Stack Overflow Questions With Partially Labeled Dirichlet Allocation
<h4 id="creators">By: Benjamin Xue, Ripudh Mylapur, Siddharth Vyasabattu, and Nicole Reardon</h4>
<h5><em> The dataset that was used for this project can be found here: <a href = "https://www.kaggle.com/datasets/imoore/60k-stack-overflow-questions-with-quality-rate">kaggle.com</a></em></h5>

<h2><strong>Introduction</strong></h2>

<p>Stack Overflow is an exchange forum where individuals can ask and answer programming-related questions. All of the posts are labeled by users with one or more tags that indicate the topic of the post and its relevance to certain programming languages and/or ideas. We would like to use the text to assign a tag to the Stack Overflow posts that fit each one the best.</p>

<h2><strong>Question</strong></h2>
<h4><strong>Can we automatically determine which tag fits the post best given the text of the post?</strong></h4>

<h2><strong>Exploratory Data Analysis</strong></h2>
<iframe src="Number of Posts from December 2015 - March 2020.html" width=800 height=600 frameBorder=0></iframe>
<iframe src="Count of the Most Common Tags.html" width=800 height=600 frameBorder=0></iframe>
<iframe src="Bar Graph Visualizing the Distribution of the Most Common Tags per Month.html" width=800 height=600 frameBorder=0></iframe>

<h2><strong>Dataset</strong></h2>
<p>The dataset we are using contains 60,000 rows of Stack Overflow posts which include:</p>
<ul>
  <li><strong><code>Id</code>:</strong> A unique integer to identify each post</li>
  <li><strong><code>Title</code>:</strong> Typically contains a concise summary of the post</li>
  <li><strong><code>Body</code>:</strong> The main portion of the post that contains the question and/or problem, sometimes including code snippets, error messages, and or expected behaviors</li>
  <li><strong><code>Tags</code>:</strong> Labels to categorize posts by topics, programming languages, or ideas</li>
  <li><strong><code>CreationDate</code>:</strong> The date and timestamp of when the post was created</li>
  <li><strong><code>Y</code>:</strong> one of three categories - <code>HQ</code>, high-quality posts that have not been edited, <code>LQ_EDIT</code>, low-quality open posts that have a negative score and have been edited, <code>LQ_CLOSED</code>, low-quality closed posts that have not been edited</li>
</ul>

<h2><strong>Data Cleaning</strong></h2>
<p>Techniques used to clean the <code>Title</code> and <code>Body</code> columns of the dataset:</p>
<ul>
  <li>Extracted code into a separate column labeled <code>Code</code></li>
  <li>Removed other HTML tags</li>
  <li>Removed any unnecessary whitespace</li>
  <li>Removed punctuation from all text</li>
  <li>Made every letter lowercase</li>
  <li>Removed any stopwords that are common throughout all documents</li>
</ul>
<p>The cleaned columns were assigned to new columns labeled <code>Title_processed</code> and <code>Body_processed</code>, respectively. The <code>Tags</code> column was also converted from a string to a list of tags.</p>

<h2><strong>Method</strong></h2>

<h2><strong>Results</strong></h2>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: left;">
      <th>DataFrame</th>
      <th>Training Accuracy</th>
      <th>Testing Accuracy</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Overall</strong></td>
      <td>__%</td>
      <td>__%</td>
    </tr>
    <tr>
      <td><strong>No Code</strong></td>
      <td>082.85%</td>
      <td>41.80%</td>
    </tr>
    <tr>
      <td><strong>Has Code</strong></td>
      <td>87.60%</td>
      <td>45.75%</td>
    </tr>
    <tr>
      <td><strong>High Quality</strong></td>
      <td>86.11%</td>
      <td>36.70%</td>
    </tr>
    <tr>
      <td><strong>Low Quality Closed</strong></td>
      <td>87.94%</td>
      <td>46.10%</td>
    </tr>
    <tr>
      <td><strong>Low Quality Edited</strong></td>
      <td>__</td>
      <td>__</td>
    </tr>
  </tbody>
</table>

<h2><strong>Findings</strong></h2>

<h2><strong>Future Work</strong></h2>

<h3>References</h3>
<ul>
<li>Ramage, D., Manning, C. D., & Dumais, S. (2011, August). Partially labeled topic models for interpretable text mining. In Proceedings of the 17th ACM SIGKDD international conference on Knowledge discovery and data mining (pp. 457-465). ACM.</li>
<li>Kapadia, Shashank. “Topic Modeling in Python: Latent Dirichlet Allocation (LDA).” Medium, 23 Dec. 2022.</li>
<li>Ramage, Daniel, et al. “Labeled Lda.” Proceedings of the 2009 Conference on Empirical Methods in Natural Language Processing Volume 1 - EMNLP ’09, 2009.</li>
</ul>

<style> 
	table{ 
		table-layout: fixed; 
		border-collapse: collapse;
		width: 100%;
        margin-right:60%;
        overflow: scroll;
		/*width: 100; 
		height:350px;*/ 
	 }
	 th{
	 	width:150%;
	 	overflow: auto;
  	white-space: nowrap;
	 }
     /* tr{
         page-break-inside: avoid;
     } */

	 td{ 
	 	overflow: auto;
	 	white-space: nowrap;
    word-wrap: break-word;
	 	width: 200%;

	 	/*width:60%;
	 	overflow: hidden;*/
/*    	white-space: nowrap;*/
	  }
    #creators{
      color: black;
    }
	sup {
	        vertical-align: super;
	        font-size: small;
	    }
</style>
