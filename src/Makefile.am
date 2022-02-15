dist_bin_SCRIPTS =
dist_bin_SCRIPTS += doit

sysconf_DATA =
sysconf_DATA += doit.conf

pkgdata_DATA =
pkgdata_DATA += doit.sh


install-exec-hook:
	sed -i 's|__LIBDIR__|$(pkgdatadir)|' $(DESTDIR)$(bindir)/doit
	sed -i 's|__CONFDIR__|$(sysconfdir)|' $(DESTDIR)$(bindir)/doit
