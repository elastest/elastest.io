# Introduction
The elastest.io web is generated with [Jekyll](https://jekyllrb.com/).

You can edit any page with a simple text editor. When you commit the changes to the repository, the web page will be updated automatically.

# How to add a new blog post
1. Clone this repository
```
git clone git@github.com:elastest/elastest.io.git
```
2. Create a new **.markdown** file into /blog/_posts folder with the following name structure:
```
YYYY-MM-DD-title.markdown 
```
3. Add the following header into file:
```
---
layout: post
title:  "Title"
date:   YYYY-MM-DD HH:MM:SS +0100
main-image: "/path/to/image"
image-alt: "image alt text"
---
```
Where you will have to set **title, date, main-image and image-alt variables**. Don't edit neither layout variable nor +0100 in date variable (GMT+1). The date can not be greater than the current date.
```
*Notes: 
Add post images into /blog/images folder.
Insert main-image path begining with slash "/".
```
4. Write post content below, in [Markdown format](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
5. If you want to preview the changes in local before commiting, you can execute the following command in the root folder of the repository (you need [Docker] installed) and open the browser in `http://localhost:4000`:

```
docker run --rm --name jekyl-elastest-docs --volume=$PWD:/srv/jekyll -p 4000:4000 -it jekyll/jekyll jekyll serve
```
6. To update the web page, commit and push your changes. Then, GitHub will update the web [elastest.io](http://elastest.io) automatically.



# Add documentation
The elastest.io documentation is generated with [MkDocs](http://www.mkdocs.org).

**To add documentation go to [elastest.io-docs project](https://github.com/elastest/elastest.io-docs)**
