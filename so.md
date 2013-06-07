up vote 5 down vote
	

1. Checkout the gh-pages branch.
2. mkdir _layouts
3. move index.html to _layouts
4. edit _layouts/index.html replace the the inner html of the contents section with {{content}}
5. make new file index.md
6. Paste markdown content of automatic page generator into index.md
7. prepend the following to index.md
```
---
layout: index
---
```
8. create _config.yml
9. include the following in _config.yml:
```
markdown: redcarpet
```
*this step is to match github's markdown syntax*
10. add & commit changes, and then push branch back to github.

Now you can simply edit index.md from the [gh-branch](https://github.com/lviggiano/owner/tree/gh-pages) in your github source browser and it will update using jekyll automatically and not mess with anything in your gh-branch.

You can also make more items editable in the layout using place holder {{page.varname}} and then adding varname:your text to the header of your index.md.
