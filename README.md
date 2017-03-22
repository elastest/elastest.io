# Installation
1. Clone or download repository
2. Install Docker
3. Open terminal and go to repository
4. Run the following command:
	```
	sudo docker run --rm --label=jekyll --volume="$(pwd)":/srv/jekyll -it -p 127.0.0.1:4000:4000 jekyll/jekyll bundle exec jekyll serve
	```
5. Open http://127.0.0.1:4000/ in your browser to view web locally


# Add new blog post
1. Create a new **.markdown** file into /blog/_posts folder with the following name structure:
	```
	YY-MM-DD-title.markdown 
	```
	
2. Add the following header into file:

		---
		layout: post
		title:  "Title"
		date:   YYYY-MM-DD HH:MM:SS +0100
		main-image: "/path/to/image"
		image-alt: "image alt text"
		---

	Where you will have to set **title, date, main-image and image-alt variables**. Don't edit neither layout variable nor +0100 in date variable (GMT+1).
	> *Note: Add post images into **/blog/images folder**
	
3. Write post content below, in markdown language


# Add documentation
The elastest.io documentation is generated with [MkDocs](http://www.mkdocs.org).

**To add documentation go to [elastest.io-docs project](https://github.com/elastest/elastest.io-docs)**