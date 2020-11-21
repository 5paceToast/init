Toast's Init Scripts
====================

Various convenience init scripts, organized by-service.
Each service directory may contain a README with additional information.
Most of these will be optimized to use with the bin bucket (see my binbuilder repository).

In general, though:

## OpenRC
Scripts will be named `$NAME.initd` and `$NAME.confd`.
They should go into `/etc/init.d/$NAME` and `/etc/conf.d/$NAME` respectively.
`$NAME` will generally be just the service name.
Some init scripts can be linked to `$NAME.$var`. This will usually be mentioned.
These scripts will use the regular (non-pathed) binary name. Feel free to modify them to point to an absolute location.

## Systemd
Scripts will be named `$NAME.service`.
Sometimes, a `$NAME2.timer` may accompany them if appropriate.
All of these should go either in `/etc/systemd/system`, `/etc/systemd/user` or `~/.config/systemd/user` directories (depending). Assume the first unless otherwise specified.
Sometimes, they will use an external configuration file. In this case, it will generally be mentioned.
