# Testing the releases of scikit-fem

![release tests](https://github.com/kinnala/scikit-fem-release-tests/workflows/release%20tests/badge.svg)

This repo is used to run the tests of kinnala/scikit-fem using PyPI releases on
Ubuntu, macOS and Windows.  See Actions for more information.

## Steps to release

In kinnala/scikit-fem:

1. Make sure that changelog in README.md is up-to-date because it gets uploaded
   to PyPI.
2. Modify the version number in setup.cfg.
3. Create a commit, e.g., "Bump up version number".
4. Push the commit and wait for the CI to run successfully.
5. Tag the commit with the new version and push the tags.
6. Run `make release` and insert PyPI username/password.
7. Using the previously created tag, draft a new release in Github to store the
   repo in Zenodo.

In kinnala/scikit-fem-release-tests:

1. Add the new release version number to `.github/workflows/main.yml`.
2. Push and check that the CI job runs successfully.
3. If not, fix the issue and go back to the beginning.
