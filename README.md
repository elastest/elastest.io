# Local Installation
1. Clone or download repository
2. Install Docker
3. Open terminal and go to repository
4. Run the following commands:
```
sudo docker run --rm --label=jekyll --volume="$(pwd)":/srv/jekyll -it -p 127.0.0.1:4000:4000 jekyll/jekyll /bin/bash
```
```
bundle install
```
```
bundle exec jekyll serve
```
5. Open http://127.0.0.1:4000/ in your browser to view web locally


# Add documentation
To add documentation go to [elastest.io-docs project](https://github.com/elastest/elastest.io-docs)
