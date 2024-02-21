+++
title = "Writing a basic EPUB viewer"
slug = "epub"
description = "Understanding the EPUB file format by writing a simple viewer."
date = "2024-02-17" 

[taxonomies]
categories = ["project"]
tags = ["epub", "rust", "gui", "iced"]

[extra]
toc = true
+++

# Prefix
I've always been an avid reader, and specifically enjoy using my Amazon Kindle. It used to be that Amazon had a couple of proprietary formats, namely Mobi and AZW.  
They've recently decided to move to the EPUB format, which is an open and widely used standard. 

As I read this, I started wondering what EPUB files actually look like, and thought that making a simple viewer for them would be a great way to learn about the format.

So without further ado, let's get started!
[EPUB 3.3 specification](https://www.w3.org/TR/epub-33/)
{% alert(title="Note:", type="info") %}
To get the full information on the EPUB format, I recommend reading the [EPUB 3.3 specification](https://www.w3.org/TR/epub-33/).
{% end %}

# What is an EPUB file?
EPUB is a file format for digital books. It's based on XML and can contain text, images, and metadata.  
It is essentially a ZIP file (formally called the *EPUB container*) with a specific structure: 
{{img(src="/assets/1_epub/epub.svg", title="EPUB structure", width="100%", maxwidth="550px", center=true)}}