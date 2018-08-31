# revel-doc on GitHub Pages

<https://helphi.github.io/pages-revel/index.html>

---

```sh
sudo apt-get install ruby ruby-dev
sudo gem install jekyll kramdown jekyll-redirect-from octopress-escape-code
git clone https://github.com/revel/revel.github.io.git
cd revel.github.io
sed -i "s#{{ page.root }}#/pages-revel#g" _includes/*.html
sed -i "s#{{ page.root }}#/pages-revel#g" _layouts/*.html
jekyll build
wget https://code.jquery.com/jquery-2.1.3.min.js -P _site/js/
sed -i "s#//ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js#/pages-revel/js/jquery-2.1.3.min.js#g" _site/index.html
rm -rf _site/README.md
cd ../
mv revel.github.io/_site/* ./
rm -rf revel.github.io
```
