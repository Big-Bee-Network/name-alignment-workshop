---
title: "What do these resolutions actually mean?"
teaching: 10
exercises: 10
questions:
- "How should I read the output given by the name-alignment-tool?"
- "Which is the "correct" name alignment?"
- "What if a name isn't matching to any of the catalogues?"
objectives:
- "Understand how to interpret the name-alignment output"
- "Understand the basics in how names are aligned, and how this can impede resolution"
keypoints:
- "Resolution is subjective to the catalogue, therefore the aligned names should be treated as hypotheses rather than true standards"
- "Name matching with the name-alignment-tool is accurate yet naive, the tool won't attempt to interpret mistakes"
---

## Interpreting the output

> So we now have our output table, but what does all of it mean? 
> [insert jpeg] 
> The field parsedName represents the scientificName field we provided in our input to the tool.
> The field parsedName represents the scientificName after undergoing parsing, parsing is a process where extranoeous information is truncated out of the name if a matching scheme supports it (e.g. Authorship/Authority) 
> the field alignRelation can have three possible values: HAS_ACCEPTED_NAME, SYNONYM_OF, or NONE. If a name is matched and is up to date/current the output will be HAS_ACCEPTED_NAME. If a name is matched, but has been identified as synonymous to another name the output will be SYNONYM_OF. This is usually the case when the original name is no longer considered taxonomically valid, and has been aligned with another species. Finally NONE indicates that there was no match found in that particular catalogue. 
> the field alignedExternalId indicates the catalogue the name was matched to. These are often abbrievated containing the ID or url within the catalogue to reference that name alignment. 
> the field alignedName is the name relation matched to the providedName. 
> the field alignedRank is the taxonomic level of the alignedName (i.e. Genus, species, etc)
> the field alignedPath shows a 'piped' list of the alignedNames taxonomic designation. (Domain | Kingdom | Phylum | Class | Order | Family | Genus | Species)

## So...what if we have different resolutions for an alignedName?
> As you might expect, not every catalogue has the same criteria for what is a species/what species are considered synonymous! 
> How you interpret these alignedNames is largely up to you as a curator/biologist/researcher. Some things worth considering are: 
> 1. What are the preferred catalogues for my field? Its often the case that taxonomic catalogues designed for particular clades/groups (e.g. DiscoverLife) are considered more accurate then broader catalogues (e.g. Catalogue of Life). 
> 2. What is the geographic extent of my collection? Some catalogues are designed with a particular area in mind. For example, the Jepson catalogue for vascular plants in California is a standard when working with California plants, but not recommended outside of the state boundaries. 
> 3. At the end of the day these names are all working hypotheses! What is an accepted name today may be a synonym of another name in the future. Keep an open mind about these interpretations. 

## NONE in the relationName field 
> While it should be expected that a name isn't in every catalogue, if you recieve no relation "NONE" for a name in all of the catalogues that could indicate something is wrong with that name. 
> To troubleshoot this its worth considering how exactly these names are aligned. NOMER the command line process that our name-alignment-tool is pulling from using an exact character matching scheme to match the providedName against the registered name in the catalogue. In English, this means the inputted name must be exactly the same as the one registered with the catalogue it is matching against. A scientific name is considered a string of characters, and if any of these characters (including spaces, punctuation, etc) are differnt between the provided and resgisterd name then the match will fail. This means that any misspellings, rougue punctuation, or whitespace will trip resolution to fail! This is part of what we mean by name matching being accurate yet naive, the tool can only work with what is provided and does not interpret intention.
