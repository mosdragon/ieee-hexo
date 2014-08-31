The New Georgia Tech IEEE Site
==============================

We now use the [Hexojs blogging framework](https://github.com/hexojs/hexo) to generate and deploy the static HTML content from simple Markdown documents.

Here is the new workflow for how new posts will be added to the site:

1. Post will be written in Markdown [here](http://markable.in/editor/)
2. The following terminal commands will be executed:
  ```
  git clone https://github.com/mosdragon/ieee-hexo
  cd ieee-hexo
  git pull origin master
  npm install
  hexo new <post-title>
  ```
  git clone https://github.com/mosdragon/ieee-hexo
  cd ieee-hexo # git pull origin master if you didn't need to clone
  npm install
  hexo new post post-title
  ```
3. Open _source/_posts/post-title.md_ in a text editor and paste Markdown from __Step 1__

4. Modify the title, then select one of the four categories: _Innovation_, _Hardware_, _General_, or _Tutoring_. Add tags for references to specific teams or designated categories such as 'workshop' or 'tech talk'. Ex:
  ```
  title: Microsoft Tech Talk and Resume Workshop Next Tuesday
  date: 2014-08-30 12:00:00
  tags: [Workshop, Tech Talk]
  categories: [General]
  ```
5. Place any images included in post in the _source/_posts/post-title/_ folder. Wherever the picture is needed in the post, place the following snippet of code <br/>
  ```
  <img src="post-title/img-name.png">
  ```
6. Preview changes locally by running the following terminal command:
  ```
  hexo server
  ```
Then go to [localhost:3000](localhost:3000) in a browser to preview your changes.

7. When all changes work and __NOTHING__ is broken, run the following:
  ```
  git add source/_posts
  git commit -m "<post-title> by <author-name>"
  git push origin <author-name>
  hexo deploy # Enter the password I gave you here
  ```

8. Changes will go live immediately on the [site](https://ieee.gatech.edu). You must, however, make a merge request from your branch to master on [GitHub](https://github.com/mosdragon/ieee-hexo) to ensure your changes stay in place when the next post is created.
