# template
If you change template.html name or script.js name then adjust in webpack.config.js

terminal scripts:
npm run dev - webpack serve i.e will host web page on http://localhost:8080/
npm build - webpack i.e bundle
npm deploy - "git subtree push --prefix dist origin gh-pages" i.e change git page

deploy correct page:
1) git branch gh-pages
2) git checkout gh-pages && git merge main --no-edit
3) npx webpack
4) git add dist -f && git commit -m "Deployment commit"
5) npm deploy
6) git checkout main

set up .gitignore with:
node_modules
dist
