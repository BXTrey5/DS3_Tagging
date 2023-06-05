# Automated Tagging of Stack Overflow Questions With Partially Labeled Dirichlet Allocation
<h4 id="creators">By: Benjamin Xue, Ripudh Mylapur, Siddharth Vyasabattu, & Nicole Reardon</h4>
<h5><em> The dataset that was used for this project can be found here: <a href = "https://www.kaggle.com/datasets/imoore/60k-stack-overflow-questions-with-quality-rate">kaggle.com</a></em></h5>

<h2>Introduction</h2>

<p>Stack Overflow is an exchange forum where individuals can ask and answer programming-related questions. All of the posts are labeled by users with one or more tags that indicate the topic of the post and its relevance to certain programming languages and/or ideas. We would like to use the text to assign a tag to the Stack Overflow posts that fit each one the best.</p>

<h2>Question</h2>
<h4><strong>Can we automatically determine which tag fits the post best given the text of the post?</strong></h4>

<h2>Exploratory Data Analysis</h2>


<h2>Dataset</h2>
<p>The dataset we are using contains 60,000 rows of Stack Overflow posts which include:</p>
<ul>
  <li><strong>Id:</strong> A unique integer to identify each post</li>
  <li><strong>Title:</strong> Typically contains a concise summary of the post</li>
  <li><strong>Body:</strong> The main portion of the post that contains the question and/or problem, sometimes including code snippets, error messages, and or expected behaviors</li>
  <li><strong>Tags:</strong> Labels to categorize posts by topics, programming languages, or ideas</li>
  <li><strong>CreationDate:</strong> The date and timestamp of when the post was created</li>
  <li><strong>Y:</strong> one of three categories - HQ, high-quality posts that have not been edited, LQ_EDIT, low-quality open posts that have a negative score and have been edited, LQ_CLOSED, low-quality closed posts that have not been edited</li>
</ul>

<h2>Data Cleaning</h2>
<p>Techniques used to clean the Body column of the dataset:</p>
<ul>
  <li>Extracted code into a separate column</li>
  <li>Removed other HTML tags</li>
  <li>Removed any unnecessary whitespace</li>
  <li>Removed punctuation from all text</li>
  <li>Made every letter lowercase</li>
  <li>Removed any stopwords that are common throughout all documents</li>
</ul>
<p>The Tags column was also converted from a string to a list of tags.</p>

<h2>Method</h2>

<h2>Results</h2>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: left;">
      <th>Subset</th>
      <th>Training Accuracy</th>
      <th>Testing Accuracy</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Overall</td>
      <td>__</td>
      <td>__</td>
    </tr>
    <tr>
      <td>No Code</td>
      <td>45</td>
      <td>12</td>
    </tr>
    <tr>
      <td>Has Code</td>
      <td>40</td>
      <td>6</td>
    </tr>
    <tr>
      <td>High Quality</td>
      <td>120</td>
      <td>7</td>
    </tr>
    <tr>
      <td>Low Quality Closed</td>
      <td>90</td>
      <td>17</td>
    </tr>
    <tr>
      <td>Low Quality Edited</td>
      <td>90</td>
      <td>17</td>
    </tr>
  </tbody>
</table>

<h2>Findings</h2>

<h2>Future Work</h2>

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
		width: 150%;
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
/*    	white-space:nowrap;*/
	  }
	  body{
	  	font-family: Helvetica, Sans-Serif;

	  }
    h1{
      font-family: Helvetica, Sans-Serif;
      color:#4B7A5C;
     }
    h4{
      color:#699A7B;

    }
    #creators{
      color: black;
    }

	sup {
	        vertical-align: super;
	        font-size: small;
	    }


</style>
