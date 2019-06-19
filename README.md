To use these:

- clone this repo into `~/.git_template`
- check that `~/.git_template/hooks/pre-commit` exists
- make sure your `~/.gitconfig` contains:
    ```
    [init]
    templatedir = ~/.git_template
    ```

Now anytime you checkout a repo OR use git init in a directory, the 
`prepare-commit-msg` hook will be copied into your project’s 
`.git/hooks` folder.

ⓘ Tip: You can safely run `git init` at the root of pre-existing git
  projects to get the template hooks copied over.


# [`prepare-commit-msg`](https://github.com/r-k-b/git-hook-templates/blob/master/hooks/prepare-commit-msg)

This commit hook will extract a Jira issue key from your branch name 
_(you are naming your branches with issue keys, aren't you?)_ and append 
it to all commit messages so that many places across our products can 
glue commits together with issues.


# [`pre-commit`](https://github.com/r-k-b/git-hook-templates/blob/master/hooks/pre-commit)

This one is for preventing yourself from accidentally committing files
that you want to change, but not commit.

Add the text `DO_NOT_COMMIT_THIS` to such files, then any commit
including that file will not succeed.
