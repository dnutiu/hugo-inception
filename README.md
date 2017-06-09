TODO: Say something about this.
Too lazy to do it right now.


## Github deployment

The tutorial section on GitHub deployment23 describes a rather complex approach using Git subtrees. There are two much simpler approaches which I thought are worth sharing.

This is based on the assumption that you are using a project page (no user or organization page, see here12 for the difference) and that your remote is called "upstream".

Publish from /docs folder on master branch
As described9 in the GitHub Pages docs, you can deploy from a folder called docs on your master branch. This requires to change the Hugo publish directory in the site config:

publishDir: "docs"
After running hugo, push your master branch to the upstream repo and choose the docs folder as the website source ("Settings " -> "GitHub Pages" -> "Source" -> "master branch /docs folder"). If that option isn't enabled, you like haven't pushed your docs folder yet.

This is the simplest approach but requires the usage of a non-standard publish directory (GitHub Pages cannot be configured to use another directory than docs currenty). Also the presence of generated files on the master branch may not be to eveyone's taste.

Deployment to gh-pages branch
The easiest way to sync the state of the public directory with your "gh-pages" branch is to create a clone of your repo under public, commit the changes and push them to the "gh-pages" branch in your local repo:

# remove previous publication
rm -rf public
mkdir public

# clone gh-pages branch from the local repo into a repo located within "public"
git clone .git --branch gh-pages public
  
# generate
hugo
  
# commit the changes in the clone and push them back to the local gh-pages branch    
cd public && git add --all && git commit -m "Publishing to gh-pages" && git push origin gh-pages

# publish
git push upstream gh-pages
That's my preferred approach as it keeps sources and generated HTML in two different branches, uses the default public folder and also keeps the histories of source branch and "gh-pages" branch fully separated from each other (unlike the subtree approach). Don't forget to add public to your .gitignore file.

I'm using a script which does this plus a few sanity checks (work area is clean etc.) which you can find in my repo11.

Note that if you are on Git 2.5 or later, the new worktree feature can be used alternatively, avoiding the cloning of the repo:

git worktree add -B gh-pages public upstream/gh-pages
This checks out the "gh-pages" branch into public, but it's linked to the local repo. I.e. if you commit the changes in public that affects the local "gh-pages" branch directly, no further push is needed.