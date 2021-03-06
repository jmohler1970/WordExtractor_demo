# WordExtractor_demo
We are going to be extracting out HTML from a Word (`.docx`) file.

`.docx` is an example of an **Open Document Format for Office Applications (ODF)** file. It is a ZIP of an XML document.

By unzipping the file and locating the appropriate XML file, we can process the data an generate HTML

# Usage

Create object, and run the main function

```
     objExtract = new wordextractor.wordextractor();

     result = objExtract.extractDocx("#strPath##fileinfo.serverfile#");

```


# Theory of Operation

There are two main ideas that make this work

1. `.docx` files are zips of xml. We will be using that as a basis open the `.docx`.
2. The xml inside of the `.docx` is highly recursive. Much like how in Twitter Bootstrap there are `<div>`s, `</div>`s, and more `</div>`s. `.docx` is in a similar structure.

## Opening a ZIP

Let's dive into some code


# Recursive Text Extractor

Let's do some recursion. For those that don't know what recursion is, you must first understand recursion before you can understand recursion (sorry)

The xml in a docx file is a nexted structure. At any give point in the structure, one of two things are going on. 

1. Either you are at tag that controls how the subordinate tags work, OR
2. You are at a tag with content.

The tags with content are easy. Just extract the content from `.xmlText` and return it.

The control and the suborinate ones are tougher to deal with.

Control means that you are in Header, or a list, or bold, or italic, or something. So you have to use that knowledge to come up with the right additional tags

Subordiante means you have to call the same function `ReadNode()` all over again. This allow you to get as deep as you need to get the content.


# Let's do some code review



# Resources

- https://en.wikipedia.org/wiki/OpenDocument

- https://helpx.adobe.com/coldfusion/cfml-reference/coldfusion-tags/tags-u-z/cfzip.html

- https://helpx.adobe.com/coldfusion/cfml-reference/coldfusion-functions/functions-t-z/xmlparse.html
