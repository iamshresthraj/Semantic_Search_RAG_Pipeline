<h1 align="center">Semantic Search and RAG Pipeline for Product Reviews</h1>

<p align="center">
A Semantic Search and Retrieval-Augmented Generation (RAG) system built using Sentence Transformers, FAISS, and FLAN-T5 to analyze Flipkart product reviews.
</p>

<hr>

<h2>Project Overview</h2>

<p>
Traditional keyword-based search systems often fail when users express their intent using different words than those stored in the database. For example, a user searching for "energy-efficient AC" might not find products labeled as "low-power air conditioner", even though both refer to the same concept.
</p>

<p>
This project addresses that problem by implementing a Semantic Search and Retrieval-Augmented Generation pipeline that retrieves relevant product reviews based on meaning rather than exact keyword matches.
</p>

<p>
The system converts product reviews into vector embeddings using Sentence Transformers and stores them in a FAISS vector index for fast similarity search. When a user submits a query, the system retrieves the most relevant reviews based on semantic similarity. The retrieved reviews are then used as context for a FLAN-T5 language model to generate a natural language answer.
</p>

<hr>

<h2>Key Features</h2>

<ul>
<li>Text preprocessing and cleaning of product reviews</li>
<li>Semantic embeddings using Sentence Transformers (all-MiniLM-L6-v2)</li>
<li>Fast vector similarity search using FAISS</li>
<li>Retrieval-Augmented Generation using FLAN-T5</li>
<li>Evaluation using Precision@K and Recall@K</li>
<li>Exploratory Data Analysis with visualizations</li>
</ul>

<hr>

<h2>Exploratory Data Analysis</h2>

<p>The project includes multiple data analysis visualizations to understand the dataset:</p>

<ul>
<li>Rating distribution</li>
<li>Word cloud of frequently used words</li>
<li>Review length distribution</li>
<li>PCA visualization of embeddings</li>
</ul>

<hr>

<h2>Technology Stack</h2>

<ul>
<li>Python</li>
<li>Sentence Transformers</li>
<li>FAISS</li>
<li>HuggingFace Transformers</li>
<li>FLAN-T5</li>
<li>Pandas</li>
<li>NumPy</li>
<li>Matplotlib</li>
<li>Seaborn</li>
<li>Scikit-learn</li>
</ul>

<hr>

<h2>Dataset</h2>

<p>
Dataset used: Flipkart Product Customer Reviews Dataset
</p>

<ul>
<li>More than 100,000 product reviews</li>
<li>Includes product name, rating, review text, and summary</li>
<li>Domain: E-commerce product reviews</li>
</ul>

<hr>

<h2>Pipeline Architecture</h2>

<ol>
<li>Data Cleaning and Preprocessing</li>
<li>Embedding Generation using Sentence Transformers</li>
<li>Vector Indexing using FAISS</li>
<li>Semantic Search to retrieve relevant reviews</li>
<li>Retrieval-Augmented Generation using FLAN-T5</li>
<li>Evaluation using Precision@K and Recall@K</li>
</ol>

<hr>

<h2>Evaluation Metrics</h2>

<p>The retrieval system is evaluated using:</p>

<ul>
<li>Precision@K</li>
<li>Recall@K</li>
</ul>

<p>
Evaluation is performed for multiple values of K = 1, 3, 5, 10.
</p>

<hr>

<h2>Business Insights</h2>

<p>
Analysis of the product reviews shows that customers frequently mention battery life, product quality, durability, and value for money. Positive reviews highlight good performance and strong battery backup, while negative reviews often focus on product defects, packaging issues, or performance not meeting expectations.
</p>

<p>
Semantic search enables users to retrieve relevant reviews even when different wording is used. For example, a query such as "long battery life" can retrieve reviews mentioning "battery backup" or "battery performance". The RAG pipeline further improves usability by generating concise summaries from multiple reviews, allowing users to quickly understand overall customer feedback.
</p>

<p>
Such systems can improve product search on e-commerce platforms, enhance recommendation systems, and help businesses monitor customer feedback more effectively.
</p>

<hr>

<h2>Future Improvements</h2>

<ul>
<li>Use larger embedding models for better semantic understanding</li>
<li>Implement hybrid search combining keyword and semantic search</li>
<li>Deploy the system as a web application</li>
<li>Integrate product recommendation capabilities</li>
</ul>

<hr>

<p align="center">
⭐ If you find this project useful, consider starring the repository.
</p>
