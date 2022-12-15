---
title: "Introduction"
teaching: 10
exercises: 0
questions:
- "Why standardize our taxonomic collections?"
- "What tools should we use to standardize our collections?"
objectives:
- "Understand that there are a lot of catalogues available for standardizing taxonomy"
- "Understand that there are multiple tools available for name alignment"
keypoints:
- "Choosing your catalogue to align your collection's names to is important!"
- "The name-alignment-tool is an option that requires no programming experience and reduces overhead that scripting languages are prone to"
---


### What is Taxonomic Name Alignment?
-----
> Taxonomic name alignment is a method we can use to standardize the scientific names of specimens in our collections to the most up to date taxonomy as listed in a authority of choice. 



### What Taxonomic Resources can we use to Align Names? 
-----
> Talk about the various catalogues available with images:: ITIS, COL, DiscoverLife, GBIF, WFO, ETC...

<img src="../fig/catalogues-logos.png" height="300" align="middle" />

> What we choose to align our names to depends on...species concept (who collected your specimens and labeled them?), geographic range of collection, and more?

### What tools are available for dealing with large quantities of names in collections?
-----
> Many! [insert some jpegs] However, alot of these are difficult to get started with without prior knowledge of programming and API calls. Scripting languages such as R also suffer from overhead making aligning thousands of names take a significant amount of time!

> The name-alignment-tool created by Jorrit offers the advantage of accessing the capabilities of the command line tool Nomer through the github interface. Meaning that you can align names without any programming experience with the speed offered by command line matching. 

-----


----


### This does mean that you need to have some knowledge of Github's interface, which is up next!
-----
> Exploratory, interactive queries can be executed through SPARQL and Cypher endpoints, GloBI Search/Browse pages, or by using the REST-y GloBI Web API. For those that use R, rglobi is available to explore interaction data. rglobi can also be used to execute Cypher queries. However, it is best to consider these as methods for exploring data rather than data access points. **If you are doing research, download the full dataset and create a version of it**.

> ## `Discussion: Why is it important to version the GloBI data in research?`
> Take a moment to discuss as a group why it is important to version, publish, or archive a copy of the GloBI dataset you use for research. What are some ways to archive datasets?
{: .discussion}

## Next Up: Light Introduction to Github

If you'd like to follow along while working with the entire dataset, please jump to [Working with the Whole Dataset](../03-ixodes-whole-dataset). 

If you would like to explore GloBI data through the GloBI webpage, please visit lesson episode [Point and Click](../04-ixodes-point-and-click).



