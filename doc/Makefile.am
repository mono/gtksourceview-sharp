if ENABLE_MONODOC
TARGETS = gtksourceview-sharp-docs.zip gtksourceview-sharp-docs.tree gtksourceview-sharp-docs.source
docsdir = `$(MONODOC) --get-sourcesdir`
docs_DATA = $(TARGETS)
else
TARGETS = 
docsdir = $(datadir)
docs_DATA =
endif


ASSEMBLER = $(MONODOC) --assemble
UPDATER = $(MONODOC) --update

gtksourceview-sharp-docs.zip gtksourceview-sharp-docs.tree: $(srcdir)/en/*/*.xml $(srcdir)/en/*.xml
	$(ASSEMBLER) --ecma $(srcdir)/en -o gtksourceview-sharp-docs

update:
		$(UPDATER) ../gtksourceview/gtksourceview-sharp.dll -o ./en -f

CLEANFILES = gtksourceview-sharp-docs.zip gtksourceview-sharp-docs.tree

EXTRA_DIST = $(TARGETS)

dist-hook:
	mkdir -p $(distdir)/en
	cp $(srcdir)/en/*.xml $(distdir)/en/
	mkdir -p $(distdir)/en/GtkSourceView
	cp $(srcdir)/en/GtkSourceView/*.xml $(distdir)/en/GtkSourceView/

