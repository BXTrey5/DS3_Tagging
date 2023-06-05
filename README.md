# Stack-Exchange-Tagging

<h2>Introduction</h2>

<p>Stack Overflow is an exchange forum where individuals can ask and answer programming-related questions. All of the posts are labeled by users with one or more tags that indicate the topic of the post and its relevance to certain programming languages and/or ideas. We would like to use the text to assign a tag to the Stack Overflow posts that fit each one the best.</p>

<h2>Question</h2>
<h4>Can we automatically determine which tag fits the post best given the text of the post?</h4>

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
<li>Extracted code into a separate column</li>
<li>Removed other HTML tags</li>
<li>Removed any unnecessary whitespace</li>
<li>Removed punctuation from all text</li>
<li>Made every letter lowercase</li>
<li>Removed any stopwords that are common throughout all documents</li>
<p>The Tags column was also converted from a string to a list of tags.</p>
