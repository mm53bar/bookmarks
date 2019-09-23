# bookmarks
A very very simple command line function making use of [Fuck Yeah Markdown](http://fuckyeahmarkdown.com)’s API to convert a given URL to a markdown formatted file.

## Usage

`kram [URL]`

Voila! The URL is converted to markdown and saved in the repo.

## Installation

Add the following to your `.bashrc`:

```
kram() { 
  output_dir=~/src/bookmarks/urls
  url=$1
  wget --quiet -O $output_dir/${url##*/}.md --post-data "u=url" http://fuckyeahmarkdown.com/go/; 
} 
