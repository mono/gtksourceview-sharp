if ENABLE_MONODOC
TARGETS = gtksourceview-sharp-docs.zip gtksourceview-sharp-docs.tree gtksourceview-sharp-docs.source
docsdir = $(prefix)/lib/monodoc/sources
docs_DATA = $(TARGETS)
else
TARGETS = 
docsdir = $(datadir)
docs_DATA =
endif

gtksourceview-sharp-docs.zip gtksourceview-sharp-docs.tree: $(srcdir)/en/*/*.xml $(srcdir)/en/*.xml
	$(MDASSEMBLER) --ecma $(srcdir)/en -o gtksourceview-sharp-docs

update:
		$(MONODOCER) -assembly:../gtksourceview/gtksourceview-sharp.dll -path:en

CLEANFILES = gtksourceview-sharp-docs.zip gtksourceview-sharp-docs.tree

EXTRA_DIST = $(TARGETS)

dist-hook:
	mkdir -p $(distdir)/en
	cp $(srcdir)/en/*.xml $(distdir)/en/
	mkdir -p $(distdir)/en/GtkSourceView
	cp $(srcdir)/en/GtkSourceView/*.xml $(distdir)/en/GtkSourceView/

