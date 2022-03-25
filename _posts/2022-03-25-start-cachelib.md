---
layout: post
title: Studying CacheLib!
excerpt: "I start blogging! I will do a series of post as I understand and configure CacheLib."
categories: [research, cache]
tags: [cachelib, cache]
comments: true
---

My research interest lies in efficiently configuring storage caches. While there are caching theories that apply across different types of caches like processor cache, web cache and storage cache, there are differences in constraints and requirements. For instance, processor caches are more sensitive to overhead compared to storage and web caches. Therefore, not all cache design and optimization techniques are translatable from one type of cache to another and configuring each type of cache has its own set of challenges. 

A large part of my struggle in graduate school has been not being able to try out my ideas for storage cache configuration on real systems and having to rely on simulations. Whether or not simulations are enough depends on the type of research. My research deals with using heterogeneous storage devices to form a cache with multiple tiers. There are complex interactions between device properties of each cache tier that influence performance apart from just cache hits. This is part of the reason why my research struggled for a long time as I was relying on simulations and analysis and making assumptions about device performance when working on multi-tier cache research. Writing my own caching system that could pass as a “real” system where ideas can be tested seemed daunting, or even impossible. 

Then, CacheLib was released by Facebook, now called Meta. It is a pluggable cache engine that is widely used in Meta. I am documenting my journey in understanding the intricacies of implementing a production level cache through my study of the CacheLib library and utilizing CacheLib to come up with efficient storage configurations (single or multi-tier) based on the workload and device properties. 


<!-- When I was looking for a theme for my website for graduate school, I wanted one with blog support. 

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

### Body text

Lorem ipsum dolor sit amet, test link adipiscing elit. **This is strong**. Nullam dignissim convallis est. Quisque aliquam.



*This is emphasized*. Donec faucibus. Nunc iaculis suscipit dui. 53 = 125. Water is H2O. Nam sit amet sem. Aliquam libero nisi, imperdiet at, tincidunt nec, gravida vehicula, nisl. The New York Times (That’s a citation). Underline.Maecenas ornare tortor. Donec sed tellus eget sapien fringilla nonummy. Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus.

HTML and CSS are our tools. Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus. Praesent mattis, massa quis luctus fermentum, turpis mi volutpat justo, eu volutpat enim diam eget metus.

### Blockquotes

> Lorem ipsum dolor sit amet, test link adipiscing elit. Nullam dignissim convallis est. Quisque aliquam.

## List Types

### Ordered Lists

1. Item one
   1. sub item one
   2. sub item two
   3. sub item three
2. Item two

### Unordered Lists

* Item one
* Item two
* Item three

## Tables

| Header 1 | Header 2 | Header 3 |
|:--------|:-------:|--------:|
| cell 1   | cell 2   | cell 3   |
| cell 4   | cell 5   | cell 6   |
|----
| cell 1   | cell 2   | cell 3   |
| cell 4   | cell 5   | cell 6   |
|=====
| Foot 1   | Foot 2   | Foot 3   |

## Code Snippets

{% highlight css %}
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
{% endhighlight %}

## Buttons

Make any link standout more when applying the `.btn` class.

{% highlight html %}
<a href="#" class="btn btn-success">Success Button</a>
{% endhighlight %}

<div markdown="0"><a href="#" class="btn">Primary Button</a></div>
<div markdown="0"><a href="#" class="btn btn-success">Success Button</a></div>
<div markdown="0"><a href="#" class="btn btn-warning">Warning Button</a></div>
<div markdown="0"><a href="#" class="btn btn-danger">Danger Button</a></div>
<div markdown="0"><a href="#" class="btn btn-info">Info Button</a></div>

## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice} -->
