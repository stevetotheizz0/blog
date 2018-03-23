---
layout: post
title: Using IPUMS data to estimate school-age children by housing type.
date: '2018-01-08'
author: Stephen Skilton
tags:
- R
- Data Wrangling

thumbnail: /img/2018-01-08.jpg

summary: The Integrated Public Use Microdata Series (IPUMS-USA) consists of more than fifty high-precision samples of the American population drawn from fifteen federal censuses and from the American Community Surveys of 2000-2012. Some of these samples have existed for years, and others were created specifically for this database. These samples, which draw on every surviving census from 1850-2000, and the 2000-2012 ACS samples, collectively constitute our richest source of quantitative information on long-term changes in the American population.

---

One of the limitations of using Census data is that when it is aggregated, it is difficult to create a picture so specific types of households. For example, recently I wanted the answer for the following question, "How many school-age children might you expect to accompany different densities of development?"

The first step to answering this would be to ask how many school-age children live in the follow types of households:

1. The families should have moved in recently, within the past 5 years?
(New construction, would probably follow a similar pattern.)
2. How many bedrooms are present in the home?
3. How many units are in the structure or is the home a single-family building?

All of these questions are present on the Census, but only in an aggregated form. What we need to do is re-aggregate individual records, filtered by 5 years, with the combination of children by bedroom and building size. Luckily IPUMS will provide samples for microdata records at geographies as small as county or the puma level.

_Note: If you don't have the expertise to sort, filter, and aggregate from a large dataset, there are other resources such as [Link to Sidney Book](sidneybook.com) that will also provide estimates._

To begin, filters are selected and downloaded from [usa.ipums.org](usa.ipums.org)
