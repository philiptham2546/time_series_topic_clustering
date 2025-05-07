# time_series_topic_clustering
Emerging tech trends: a time series topic clustering framework for early-stage venture capital decision making

This project aims to apply machine learning techniques to help tech investors in the venture capital (VC) industry identify emerging topics that could become “the next big thing.”
To do so, we designed an algorithm to detect tech topics that start small but grow over time using time‑series topic analysis. Our data consisted of text scraped from the tech‑focused news site Hacker News over seven weeks. 
We extracted topic representations with BERTopic, tracked them through time via K‑means clustering, and scored them based on investor relevance. We find that the model successfully identified dominant themes during this period—such as “Political Economy” and “Web Browsers”—but further tuning and a longer time window would be necessary to surface more specific topics with genuine investment potential.
<br>
<h2>Data scraping for HackerNews articles and comments summary</h2><br>
<b>Dependencies:</b> bs4, requests, optionally, fake_useragent<br>
<b>Parameters:</b> date range, pages per day<br><br>
<b>Usage:</b><br>
<ol>
  <li>Update the day1 and day2 params which establish beginning and ending of date range to fetch. However, multiday requests often fail, so it's better to make both days consecutive, hence why there is no param for month. </li>
  <li>Update desired output file name.</li>
  <li>Update the desired page count to fetch per day.</li>
  <li>Run cell.</li>
</ol><br>
<b>Output:</b> Text file where each row has one article title immediately followed by its comments on the HackerNews site<br>
<h2>TLDR of files</h2><br>
<ul>
  <li>aml_betopic_opt_scratch.ipynb: tuning bertopic hyperparameters (pca n_comp and hdbscan min_cluster_size)</li>
  <li>meta_cluster_identification.ipynb: stages 1 and 2 (identifying topics in each batch using bertopic, identifying meta clusters across batches using kmeans)</li>
  <li>meta_topics_cv_df.csv: cross validated meta topic representations to show model stability</li>
  <li>meta_topics_df.csv: meta topic representations</li>
  <li>top_20_tfidf_all_batches.zip: zipped 13 csv files of the top 20 words by tfidf from each batch for dumb and reasonable model evaluation</li>
</ul>
