## Before release

1. Check issue milestones to see outstanding issues to resolve if possible or transfer to the milestones for the next release e.g. [`v1.9`](https://github.com/nf-core/tools/issues?q=is%3Aopen+is%3Aissue+milestone%3A1.9)
2. Most importantly, pick an undeniably outstanding [name](http://www.codenamegenerator.com/) for the release where _Prefix_ = _Metal_ and _Dictionary_ = _Animal_.
3. Check whether the GitHub Actions workflow scripts need updating of the Nextflow versions
4. Create a PR to `dev` to bump the version in `CHANGELOG.md` and `setup.py`.
5. Make sure all CI tests are passing!
6. Create a PR from `dev` to `master`
7. Make sure all CI tests are passing again (additional tests are run on PRs to `master`)
8. Request review (2 approvals required)
9. Merge the PR into `master`
10. Wait for CI tests on the commit to passed
11. (Optional but a good idea) Run a manual sync on `nf-core/testpipeline` and check that CI is passing on the resulting PR.
12. Create a new release copying the `CHANGELOG` for that release into the description section.

## After release

1. Check the automated template synchronisation has been triggered properly. This should automatically open PRs directly to individual pipeline repos with the appropriate changes to update the pipeline template.
2. Check that the automatic `PyPi` deployment has worked: [pypi.org/project/nf-core](https://pypi.org/project/nf-core/)
3. Check `BioConda` has an automated PR to bump the version, and merge. eg. [bioconda/bioconda-recipes #20065](https://github.com/bioconda/bioconda-recipes/pull/20065)
4. Create a tools PR to `dev` to bump back to the next development version in `CHANGELOG.md` and `setup.py`
