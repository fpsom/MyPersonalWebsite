---
layout: page
title: Publications
permalink: /research/publications/
---

# Bibliography

[**Book**](#book)  |  [**Book Chapter**](#book-chapter)  |  [**Journals**](#journals)  |  [**Conferences and Announcements**](#conferences-and-announcements)  |  [**Other**](#other)

## Book

{% bibliography --query @book[key=OSTHbook] %}

## Book Chapter

{% bibliography --query @incollection[key=DataMiningProteomicsGrid] %}

## Journals

### 2020

{% bibliography --query @article[year=2020] %}

### 2019

{% bibliography --query @article[year=2019] %}

### 2018

{% bibliography --query @article[year=2018] %}

### 2017

{% bibliography --query @article[year=2017] %}

### 2016

{% bibliography --query @article[year=2016] %}

### 2015

{% bibliography --query @article[year=2015] %}

### 2013

{% bibliography --query @article[year=2013] %}

### 2012

{% bibliography --query @article[year=2012] %}

### 2010

{% bibliography --query @article[year=2010] %}

### 2009

{% bibliography --query @article[year=2009] %}


## Conferences and Announcements

### 2020

{% bibliography --query @inproceedings[year=2020] %}

### 2019

{% bibliography --query @inproceedings[year=2019] %}

### 2018

{% bibliography --query @inproceedings[year=2018] %}

### 2017

{% bibliography --query @inproceedings[year=2017] %}

### 2016

{% bibliography --query @inproceedings[year=2016] %}

### 2015

{% bibliography --query @inproceedings[year=2015] %}

### 2014

{% bibliography --query @inproceedings[year=2014] %}

### 2012

{% bibliography --query @inproceedings[year=2012] %}

### 2011

{% bibliography --query @inproceedings[year=2011] %}

### 2010

{% bibliography --query @inproceedings[year=2010] %}

### 2009

{% bibliography --query @inproceedings[year=2009] %}

### 2008

{% bibliography --query @inproceedings[year=2008] %}

### 2007

{% bibliography --query @inproceedings[year=2007] %}

### 2006

{% bibliography --query @inproceedings[year=2006] %}

### 2005

{% bibliography --query @inproceedings[year=2005] %}

### 2004

{% bibliography --query @inproceedings[year=2004] %}


## Other

### Short articles

{% bibliography --query @misc %}

### Thesis

{% bibliography --query @phdthesis %}


[//]: # {% bibliography --query @ \* [year=2017] %}
[//]: # (pandoc --filter=pandoc-citeproc --standalone publications.md -o publications.html)
