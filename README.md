# WordExtractor_demo
Demonstrates Word Extractor


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


## Recursive Text Extractor

Let's do some recursion. For those that don't know what recursion is, you must first understand recursion before you can understand recursion (sorry)



