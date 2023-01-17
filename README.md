bacula-rpm-builder
==================

This repo is intended to make it possible to build rpms directly from
the bacula git repo without necessarily waiting for the specific rpms
to be built by the upstream code owners.

Ideally this script could be incorporated into th
upstream code so that there's a clearly defined way to build rpms directly from
the git repo.  This information was missing as described in:

see:
- https://bugs.bacula.org/view.php?id=2575 (original)
- https://gitlab.bacula.org/bacula-community-edition/bacula-community/-/issues/2575
- https://bugs.bacula.org/view.php?id=2576 (original)
- https://gitlab.bacula.org/bacula-community-edition/bacula-community/-/issues/2576

I had wanted to use rpms for CentOS 9 when they were not being provided and found it
hard from the source tree to figure out exactly how to get to build the packages
provided by Bacula Systems directly from the git source tree.

This repo is my attempt to make this work for the distribution versions I use
and ideally extend the procedure to be generic.  I assume that internally
Bacula Systems are building in a similar way, but the process they use is not
shared.

The easier it is to build these rpms the more people will use them
and often the rpms provided with older distributions are much older than the
latest version of bacula.  Also if you run a storage daemon on a different
server to the director this version must match exactly or it will not work.
This was causing me trouble as I had been making copies to 2 different backends
and was unable to keep them both in sync with the latest bacula version.

Feedback and patches for this will be most welcome once things look a bit more
stable and I am able to at least make a clean build for 1 or 2 CentOS versions.

Simon Mudd
