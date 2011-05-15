
DIR = $(libdir)/yog/0.0.10
install:
	find . -name "*.yg" | while read pkg; \
	do \
		mkdir -p `dirname $(DESTDIR)$(DIR)/$${pkg}`; \
		$(INSTALL_DATA) $${pkg} $(DESTDIR)$(DIR)/$${pkg}; \
	done

# vim: tabstop=8 shiftwidth=8 noexpandtab
