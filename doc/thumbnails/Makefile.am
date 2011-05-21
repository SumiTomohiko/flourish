
resourcedir = $(htmldir)/thumbnails
resource_DATA = cave.png ending.png

IMAGES_DIR = ../images

cave.png: $(IMAGES_DIR)/cave.png Makefile
	convert -geometry 50% $(IMAGES_DIR)/cave.png cave.png

ending.png: $(IMAGES_DIR)/ending.png Makefile
	convert -geometry 50% $(IMAGES_DIR)/ending.png ending.png

# vim: tabstop=8 shiftwidth=8 noexpandtab
