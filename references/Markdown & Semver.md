# Markdown & Semver
Github guide to markdown so Zinzan stops formatting incorrectly can be found [here](https://guides.github.com/features/mastering-markdown/) :thinking:

## @ in md
You can notify a github user in the repo to see something specific by using `@<username>` 
e.g. @SzymonBgit look at this file lmao

# Tagging and Semantic Versioning
Section describes how to use `git tag` in conjuction with [CHANGELOG.md](../CHANGELOG.md).

## Semantic Versioning
e.g. `v1.3.6` - essentially a way of describing what each version does in relation to the previous.

Format is:
> **Major.Minor.Patch**

*Major release* - increment if new features break backwards compatibility/current features

*Minor release* - increment if the new features are compatible with app in current state and do not break any pre-existing features

*Patch release* - increment if fixing existing features

### Links
Overview to Semver availiable [here](https://medium.com/@jameshamann/a-brief-guide-to-semantic-versioning-c6055d87c90e) and full documentation of method [here](https://semver.org/).

## Tagging in Github
Add a Tag to your current working commit by using `git tag "vM.M.P"` and view tag history using `git tag` :
```
$ git tag v0.5
$ git tag
v0.1
v0.2
v1.0
```
Can use `-a` to create an annotated tag and supply message with `-m`. To view a tag use `git show`:
```
$ git tag -a v1.4 -m "tag message"
$ git show v1.4
commit ca82a6dff817ec66f44342007202690a93763949
Author: zzuob <(email))>
Date:   Mon Mar 17 21:52:11 2008 -0700

    tag message
```
### Pushing Tags
`git push` will not include any tags added to the commit. To push a commit with an updated tag use `git push origin <tagname>`: 
```
$ git push origin v1.5
Counting objects: 14, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (12/12), done.
Writing objects: 100% (14/14), 2.05 KiB | 0 bytes/s, done.
Total 14 (delta 3), reused 0 (delta 0)
To git@github.com:schacon/simplegit.git
 * [new tag]         v1.5 -> v1.5
 ```
 ## Links
 Guide to Tagging: https://git-scm.com/book/en/v2/Git-Basics-Tagging