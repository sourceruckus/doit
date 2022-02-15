dist_bin_SCRIPTS =
dist_bin_SCRIPTS += doit

pkgdata_DATA =
pkgdata_DATA += doit.sh


install-exec-hook:
	sed -i 's|__LIBDIR__|$(pkgdatadir)|' $(DESTDIR)$(bindir)/doit
