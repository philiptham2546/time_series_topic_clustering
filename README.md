# time_series_topic_clustering
Emerging tech trends: a time series topic clustering framework for early-stage venture capital decision making

This project aims to apply machine learning techniques to help tech investors in the venture capital (VC) industry identify emerging topics that could become “the next big thing.”
To do so, we designed an algorithm to detect tech topics that start small but grow over time using time‑series topic analysis. Our data consisted of text scraped from the tech‑focused news site Hacker News over seven weeks. 
We extracted topic representations with BERTopic, tracked them through time via K‑means clustering, and scored them based on investor relevance. We find that the model successfully identified dominant themes during this period—such as “Political Economy” and “Web Browsers”—but further tuning and a longer time window would be necessary to surface more specific topics with genuine investment potential.
