
SUBDIRS=		gtksourceview doc
EXTRA_DIST=		nemerle.lang vbnet.lang gtksourceview-sharp.pc.in $(mimeinfo_DATA) gtk-sharp.snk

extra_langdir= @gtksourceview_prefix@/share/gtksourceview-1.0/language-specs
extra_lang_DATA=	nemerle.lang vbnet.lang

pkgconfigdir = @libdir@/pkgconfig
pkgconfig_DATA = gtksourceview-sharp.pc

# should be the same as the gnome prefix
mimeinfodir = @gtksourceview_prefix@/share/mime-info
mimeinfo_DATA = gtksourceview-sharp.mime gtksourceview-sharp.keys

