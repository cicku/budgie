-include $(top_srcdir)/common.mk

budgiedir=$(datadir)/budgie
budgie_DATA = \
	album-base.png \
	album-overlay.png

# Our SVG
iconsdir=$(datadir)/icons/hicolor/scalable/apps
icons_DATA = \
	budgie.svg

# Our .desktop file
desktopdir=$(datadir)/applications
desktop_DATA = \
	budgie.desktop

# GLib Schema
glibdir=$(datadir)/glib-2.0/schemas
glib_DATA = \
	io.github.ikeydoherty.Budgie.gschema.xml

EXTRA_DIST = \
	album-base.png \
	album-overlay.png \
	budgie.desktop \
	io.github.ikeydoherty.Budgie.gschema.xml \
	budgie.svg \
	budgie-128x128.png \
	budgie-16x16.png \
	budgie-192x192.png \
	budgie-22x22.png \
	budgie-24x24.png \
	budgie-256x256.png \
	budgie-32x32.png \
	budgie-36x36.png \
	budgie-48x48.png \
	budgie-512x512.png \
	budgie-64x64.png \
	budgie-72x72.png \
	budgie-96x96.png

# Our PNG's
icon_sizes = \
	128x128 \
	16x16 \
	192x192 \
	22x22 \
	24x24 \
	256x256 \
	32x32 \
	36x36 \
	48x48 \
	512x512 \
	64x64 \
	72x72 \
	96x96 \
	$(NULL)

install-icons:
	for iconsize in $(icon_sizes); do \
		mkdir -p $(DESTDIR)$(datadir)/icons/hicolor/$$iconsize/apps; \
		$(INSTALL_DATA) $(srcdir)/budgie-$$iconsize.png $(DESTDIR)$(datadir)/icons/hicolor/$$iconsize/apps/budgie.png; \
	done
	
uninstall-icons:
	for iconsize in $(icon_sizes); do \
		rm $(DESTDIR)$(datadir)/icons/hicolor/$$iconsize/apps/budgie.png; \
	done
	
install-data-local: install-icons
uninstall-local: uninstall-icons
