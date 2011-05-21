
SUBDIRS = images thumbnails
resourcedir = $(htmldir)
resource_DATA = demo.ogg index.html

FFMPEG = ffmpeg -y

demo.ogg: demo.avi Makefile
	$(FFMPEG) -i demo.avi -vol 2048 -acodec libvorbis demo.ogg

demo.avi: demo1.avi demo2.avi Makefile
	mencoder -quiet demo1.avi demo2.avi -o demo.avi -oac copy -ovc copy

demo1.avi: attack.avi Makefile
	$(FFMPEG) -ss 1.5 -t 7.5 -i attack.avi demo1.avi

demo2.avi: stone.avi Makefile
	$(FFMPEG) -ss 2 -t 7 -i stone.avi demo2.avi

SUFFIXES = .avi .ogv

.ogv.avi:
	$(FFMPEG) -i $< -ab 16k $@

include $(top_srcdir)/Makefile.common

# vim: tabstop=8 shiftwidth=8 noexpandtab
