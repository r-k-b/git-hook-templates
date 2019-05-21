This commit hook will extract a Jira issue key from your branch name 
(you are naming your branches with issue keys, aren't you?) and append 
it to all commit messages so that many places across our products can 
glue commits together with issues.

To use this:

- make sure the folder(s) `~/.git_template/hooks` exists
- drop this file in there and make sure it’s named `prepare-commit-msg`
- make sure your `~/.gitconfig` contains:
    ```
    [init]
    templatedir = ~/.git_template
    ```

Now anytime you checkout a repo OR use git init in a directory, the 
`prepare-commit-msg` hook will be copied into your project’s 
`.git/hooks` folder.

ⓘ Tip: You can safely run `git init` within pre-existing git projects 
  to get the file copied over.
