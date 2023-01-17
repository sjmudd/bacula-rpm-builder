bacula-rpm-builder
==================

This repo is intended to make it possible to build rpms directly from
the bacula git repo in a repeatable manner without necessarily needing
to wait for them to be built by the upstream code owners.

Ideally this script could be incorporated into the
upstream code so that it is visible to more peope and they are able to use
it to build rpms directly if needed.

This information has been missing in the upstream source code as described
below:
- https://bugs.bacula.org/view.php?id=2575 (original)
- https://gitlab.bacula.org/bacula-community-edition/bacula-community/-/issues/2575
- https://bugs.bacula.org/view.php?id=2576 (original)
- https://gitlab.bacula.org/bacula-community-edition/bacula-community/-/issues/2576

While templated `.spec.in` files are provided in the git repo there was
no explanation of exactly how to convert the git tree into the required
format to build the packages.

I had wanted to use rpms for CentOS 9 when they were not being provided
and found it hard from the source tree to figure out exactly how to get
to build the needed packages directly from the git source tree.

This repo is my attempt to make this work for the distribution versions
I use and ideally extend the procedure to be generic.  I assume that
internally Bacula Systems are already building the rpms in a similar way,
but the process they use is not shared.

The easier it is to build these rpms the more people will use them.
- Additionally the rpms provided with older distributions are much
  older than the latest version of bacula so using more up to date rpms
  is good.
- The storage daemons and director MUST run exactly the same version
  and this was causing me troubles as I was backing up to 2 different
  systems to 2 different OS versions, one of which was not supported.
  Once I can build the versions myself that problem goes away.
- I also wanted to build my MySQL libraries using the official
  MySQL Community rpms and not the older system rpms provided by the
  OS vendor. Being able to build the rpms myself made this task
  possible.

Feedback and patches for this will be most welcome once things look a
bit more stable and I am able to at least make a clean build for 1 or
2 CentOS versions.

Simon J Mudd <sjmudd@pobox.com>
