---
title: "Using the name-alignment-tool"
teaching: 15
exercises: 10
questions:
- "How do I interact with this tool?"
- "How can I change the names that the tool resolves?"
- "How can I choose which catalogues to align names to? What are my catalogue options?"
- "How can I access my output? What do these outputs mean?"
objectives:
- "Understand how to navigate the tool"
- "Learn the process of adding files containing names for matching, requirements, and accessing the tool's output."
keypoints:
- "Knowing the basic steps of adding data, data requirements, changing the readme, and accessing the outputs will give you full access to the tool's aligning capabilities." 
---

## Uploading Names for Matching 

> For the tool to interact and read our files, we need either a file stored locally on this github repository or a dwc archive link. For todays demonstration lets look at how we can upload a list of names to our local directory for the github repository 

{ :Note} "Local Directories" When we say local directory we are referring to the location at which the program looks for a file. For github, your local directory isn't on your personal device but rather the files stored in your repository. For the purpose of our tutorial, this means that we need to upload files onto the github repository's local directory in order for the name-alignment-tool to interact with them. 
> 
> Download this example [name file](https://Big-Bee-Network.github.io/names.csv) containing a comma delimited file of bee names for our worked through example. 
> Take a look at the data, you'll notice that there is one field called 'scientificName' and 10 rows containing bee names in this field. This is important! When using the name-alignment-tool with data uploaded from a csv or tsv you **must** this structure, including other information will cause name alignment to fail.
> Now we're going to upload this file into the github repo, this is done by:
> 1) Click Add File, then select file to upload. Select the file from your downloads. [insert jpeg]
> 2) "Commit" is git's way of saying you are making a change to your repository. You will need to enter some sort of phrase when commiting, I usually do something short and sweet that will jog my memory if I need to go back... [insert jpeg]
> 3) You should now see the file in the Repo! This means the file is now stored locally on this github repo. [insert jpeg]

## Editing the README to Run the Tool 
> To use the tool, we are going to need to accomplish three things:
> 1) Select the file with the names we want to align
> 2) Edit the catalogues that we would like to align our names against
> 3) Commit the changes to start the process of name alignment

> We can accomplish this by editing the README, first lets select the pencil icon on your repo's README [insert jpeg]. 
> This will direct us to a screen where we can now edit the README's contents. Note that in the syntax of '#' denotes commenting a line of code out, meaning that lines with these are not run. You will notice that most cases of these are to provide notes on what is happening with the code, however we can also use it to our advantage if we want to keep what was originally written but choose not to run it. More on this later! 

>1) Selecting the file with names we want to align:
> The first chunk of information read by the tool starts with datasets: [insert jpeg]
> Changing the name of the file in the url field allows us to call the data from a local github repo to the tool. Note that the there is dummy data listed in these currently for illustration purposes that will provide outputs. 
> Notice that there are 3 options for uploading your data, and the one you choose will depend on the type of file that contains your names. There are three file types that the name-alignment-tool currently supports: csv, tsv, and darwin core archives (dwca). For this example, we are using a comma seperated value file, so we're going to replace 'foodorganisms.txt' with the name of our bee-name file.  [insert jpeg]
> We also want to make sure we aren't running the other datasets, but its nice to retain formatting for future use of the tool if your file is not a csv. Lets take advantage of commenting out lines with '#' to stop those datasets from being run. 

> 2) Edit the catalogues that we would like to align our names against
> Next we're going to navigate to the chunk below that starts with taxonomies: [insert jpeg]
> This chunk contains all of the catalogues you would like to align names against. The structure includes id: which is an **exact** name as listed on NOMER's readme and a name: which is a general name for the catalogue.[insert jpeg] [Make a warning field ! The id field **must** match the listed IDs on Nomer to correctly match, think of it as all of the catalogues being locked doors and choosing you must have a key with a perfect fit to open your doors of interest!]
> Its also apparent that there are quite a few catalogues listed here; however, not all of these catalogues are useful for resolving taxonomy in bees! An advantage of this tool is that we can align names to multiple catalogues to get comparisons. For this showcase, lets use Catalogue of Life, GBIF, and DiscoverLife bee species checklist. Two of these are already listed, however we're going to want to create a new id & name field for discoverlife. [insert jpeg]. We could run all of these, however the more catalogues you match against the longer it takes to get an output. So lets take advantage again of the commenting out the catalogues we are not interested in running with the '#'. [insert jpeg]

> 3) Commit the changes to start the process of name alignment
> Now we're ready to run the tool! Simply create a short commit message and commit changes

## Where to find the Resolution
> The tool is currently being run through Github, but we can see this in action by clicking on the orange dot [insert jpeg] 
> If you click on this, you will see the tool going through the associated steps. The details aren't super important, but know that the tool is accessing the command line tool Nomer and is then aligning our names against the catalogues. [insert jpeg]

> Once names are aligned, there are circumstances where you get a red X from resolution indicating some sort of failure in alignment. This is OK! This simply means that in one of the catalogues that we chose to match names against there wasn't an output for a certain name. This will be read as NONE for relation. [jpeg]
> [Make a warning field ! There is however an error to watch out for, called No Name Found(?). This Error is typically something to do with the formatting of the file uploaded not being read correctly. I would first check to make sure your field is labeled "scientificName" and then make sure its in the correct dataset field on the README (either .csv or .tsv). If this doesn't fix it I would look through the README to make sure something isn't accidently commented out or deleted. Remember, you create another copy of the template if you can't identify the problem!]

> Finally the aligned names will create a link, which can be accessed for a one time download. Go ahead and click the link and intiate the download. [insert jpeg]


