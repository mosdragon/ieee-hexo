The New Georgia Tech IEEE Site
==============================

The site now uses the [Hexojs blogging framework](https://github.com/hexojs/hexo) to generate the static HTML content from simple Markdown documents.

Here is the new workflow for how new posts will be added to the site:

1. Officer/Member will create a Google Doc with proposed content for the new post (title, content, images, etc)
2. The doc will be emailed/shared with the Webmaster
3. Webmaster will format content [here](http://markable.in/editor/)  and save images in a folder titled _images_
4. Webmaster will run the following commands in a terminal prompt:<br>
_(note: you will need [Node](http://nodejs.org) and the npm package [hexo](https://github.com/hexojs/hexo))_
<pre>
$ git clone https://github.com/mosdragon/ieee-hexo
$ cd ieee-hexo
$ npm install
$ hexo new post <code>post-title-here</code>
</pre>
5. Open _sources > _posts > post-title > post-title.md_ in a text editor
6. Paste markdown text from  __Step 3__ into _post-title.md_ and save
7. Copy _images_ folder from __Step 3__ into _sources > _posts > post-title > post-title_
8. From the root directory, run the following command:
<pre>
hexo clean // Erases cache and public directory, if it exists
hexo generate // Generate static HTML for site
</pre>
9. SSH or FTP into [ieee.gatech.edu](http://ieee.gatech.edu) and replace existing files with all files in the _public_ directory
