---
layout: post
title: Studying CacheLib!
excerpt: "I start blogging! I will do a series of post as I understand and configure CacheLib."
categories: [research, cache]
tags: [cachelib, cache]
comments: true
---

My research interest lies in efficiently configuring storage caches. While there are caching theories that apply across different types of caches like processor cache, web cache and storage cache, there are differences in constraints and requirements. For instance, processor caches are more sensitive to overhead compared to storage and web caches. This means that web and storage caches are more suitable for utilizing complex data management techniques with high overheads than processor caches.  

CacheLib is an open source cache engine developed by Meta. I will update CacheLib to replay block traces and evaluate their performance under various settings. The goal is to find the relationship between workload properties and cache configuation to be able to better configure a storage cache. 

I am making notes in the blog posts as I understand the library and update it. 
