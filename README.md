# How to use Octopress

## The basics

### 2 main branches

There are 2 main branches that hold production code.

* `master`: holds the source code. This is the branch you make a feature branch of and add stuff to.
* `gh-pages`: This is the branch that holds the compiled site. You never commit to this directly.

### Adding a new post

1. Clone the repo and make your own branch using `git checkout -b my_branch_name`
2. Generate a new post with `rake new_post[This is my awesome title]`
3. Edit the post using markdown
4. Preview your post as you type using `rake preview` which starts a server on port 4000 and keeps track of changes and recompiles the code.
5. When you are done commit your code to your own branch
6. Publish your own branch using `git push -u origin my_branch_name`
7. Open a pull request to get your post approved by someone. We all do spelling mistakes.

### Deploying the site

1. Pull the latest changes and checkout the master branch
2. Run `rake gen_deploy` to generate and deploy the latest code