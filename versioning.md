# Versions and Revisions

This is a brainstorming document about requirements and approaches for
versioning for keeping metadata for versioning and revisions of models.

## Base on [semver][] (Semantic versioning)

[semver]: https://semver.org/

We like being able to distinguish incompatible changes from backwards compatible
changes.  A more detailed proposal for what that might mean is in [convergence.md](convergence.md).

## Enable different groups to evolve

It should be possible for one group to take an existing version and
start revising it

* preserving information about base version
* enabling steps in the development stream
* enable incorporation in the base
* keep developer-specific information

Assigning a version numbers needs to be an explicit step on a version
stream (version track?).  E.g., just because a developer makes a
revision to OneDM version 3.4, this doesn't mean that the revision
becomes OneDM 3.4.1.  The assignment must enable parallel development
activities by different groups.  Preferably, it should enable
intermingling them.

## Enable use entirely within an organization

The versioning scheme should not depend on OneDM assigning a version
first.

# Approaches

Possibly, several items of metadata could coexist in an sdfinfo
structure.

It should be possible to determine which of these metadata is still
true (e.g., this is OneDM version 3.4 of a model) and which are
information about base versions (e.g., this is Ecosystem A's version
N.M proposal for updating OneDM version 3.4, with some proposed
updates by developer X).

