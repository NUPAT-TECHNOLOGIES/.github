## Commit Message Formats
---
### Default
<pre>
<b><a href="#type">&lt;type&gt;</a></b></font>(<b><a href="#scope">&lt;scope&gt;</a></b>): <b><a href="#description">&lt;description&gt;</a></b>
<sub>❗do not capitalise the first letter(s)</sub>
<sub>❗no period (.) at the end of description</sub>
</pre>

#### Type
* API relevant changes
   * `feat` Commits that removes or adds a new feature.
   * `fix` Commits that fixes a bug.
* `refactor` Commits that restructures code but does not change any API behaviour.
   * `perf` Special `refactor` commits that improve performance.
* `style` Commits that only affects visual elements.
* `lint` Commits that improves code quality (white-space, formatting, unused variables, missing docstrings etc).
* `test` Commits that add missing tests or correct existing tests
* `docs` Commits that affect documentation only.
* `build` Commits that affect build components like build tools, ci pipeline, dependencies, and project version.
* `ops` Commits that affect operational components like infrastructure, deployment, backup, and recovery.
* `chore` Miscellaneous commits e.g. modifying `.gitignore`.
* `Securiy` Commits that fix vulnerabilities.

#### Scope
The `scope` provides additional contextual information.
* It is an **optional** part of the commit message format.
* Don't use issue identifiers as scopes.

#### Description
The `description` contains a concise description of the change.
* It is a **mandatory** part of the format.
* Use the imperative, present tense: "change" not "changed" nor "changes"
  * Think of `This commit will...` or `This commit should...`
* Do not capitalize the first letter.
* No period (`.`) at the end.

#### Breaking Changes Indicator
Breaking changes refer to modifications to the codebase that make it incompatible with existing code that depends on it, e.g. renaming or removing a function, database schema changes, or changing the behaviour of a method.

Breaking changes should be indicated by an `!` before the `:` in the subject line e.g.
   ```
   feat(api)!: remove status endpoint
   ```
* It is an **optional** part of the commit message format.
* In the commit/PR description body, start with the word `BREAKING CHANGES:` followed by space or two newlines.
<br>
<br>

### Examples
* ```
  feat: add email notifications on new direct messages
  ```
* ```
  feat(shopping cart): add the amazing button
  ```
* ```
  feat!: remove ticket list endpoint

  BREAKING CHANGES: ticket enpoints no longer supports list all entites.
  ```
* ```
  fix(api): handle empty message in request body
  ```
* ```
  fix(api): fix wrong calculation of request body checksum
  ```
* ```
  fix: add missing parameter to service call

  The error occurred because of <reasons>.
  ```
* ```
  perf: decrease memory footprint for determining uniqe visitors by using HyperLogLog
  ```
* ```
  build: update dependencies
  ```
* ```
  build(release): bump version to 1.0.0
  ```
* ```
  refactor: implement fibonacci number calculation as recursion
  ```
* ```
  style: increase sign-up button left margin from 10px to 12px
  ```
<br>
<br>

### Additional Considerations

#### Commit/PR Description Body
The `body` should include the motivation for the change. Contrast this with a brief description of the previous behaviour.
* It is generally **optional**, but essential when creating a PR with multiple code changes.
* Use the imperative, present tense: "change" not "changed" nor "changes".
* This is the place to **reference Issues** (by id) that this commit/PR refers to.

#### Default Merge Commit
<pre>
Merge branch '<b>&lt;branch name&gt;</b>'
</pre>
<sup>Follows default git merge message</sup>

#### Default Revert Commit
<pre>
Revert "<b>&lt;reverted commit subject line&gt;</b>"
</pre>
<sup>Follows default git revert message</sup>

#### Default Inital Commit 
```
chore: init
```


---

### References
* https://www.conventionalcommits.org/
* https://github.com/angular/angular/blob/master/CONTRIBUTING.md
* http://karma-runner.github.io/1.0/dev/git-commit-msg.html
<br>

* https://github.com/github/platform-samples/tree/master/pre-receive-hooks  
* https://github.community/t5/GitHub-Enterprise-Best-Practices/Using-pre-receive-hooks-in-GitHub-Enterprise/ba-p/13863
