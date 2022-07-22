# OPI Project Development Flow

This document attempts to document the development flow as the project moves
towards code generation.

## Sub-Projects and GitHub Repositories

Each sub-project has their own GitHub Repository where they are currently
iterating on documents and some early code. We advocate that model should
continue going forward. Further, if a sub-project wants to create additional
GitHub repositories, that should be fine as well.

## The Role Of the PoC GitHub Repository

The [PoC GitHub Repository](https://github.com/opiproject/opi-poc) is
currently iterating on a full OPI proof of concept. While that work is ongoing,
we antiticpate this eventually ingesting components from other sub-projects.
For example, the PoC GitHub Repository may end up using some of the
provisioning work from the [OPI Prov GitHub Repository](https://github.com/opiproject/opi-prov-life).
In some ways, the PoC GitHub Repository becomes a system test of sorts.

## Validation Across Repositories

We expect each sub-project to have appropriate CI testing:

* Linting of various forms (markdown, code specific linting)
* Unit tests
* Functional tests
* Container builds and pushed to GitHub Container Registry

We also expect testing across repositories to work such that sub-projects can
make use of the PoC GitHub and run the PoC code as a form of system test.
