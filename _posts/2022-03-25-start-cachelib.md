---
layout: post
title: Studying CacheLib!
excerpt: "I start blogging! I will do a series of post as I understand and configure CacheLib."
categories: [research, cache]
tags: [cachelib, cache]
comments: true
---

My research interest lies in efficiently configuring storage caches. While there are caching theories that apply across different types of caches like processor cache, web cache and storage cache, there are differences in constraints and requirements. For instance, processor caches are more sensitive to overhead compared to storage and web caches. Therefore, not all cache design and optimization techniques are translatable from one type of cache to another and configuring each type of cache has its own set of challenges. 

CacheLib is a pluggable cache engine that is widely used in Meta. I am documenting myself as I understand the library in order to upgrade it for my own use. 
