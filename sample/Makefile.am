TEST = SourceViewTest.exe

EXTRA_DIST = SourceViewTest.cs
CLEANFILES = $(TEST) $(TEST).mdb

all: $(TEST)

$(TEST): $(srcdir)/SourceViewTest.cs
	$(CSC) -out:$@ $(srcdir)/SourceViewTest.cs -r:../gtksourceview/gtksourceview-sharp.dll -pkg:gtk-sharp-2.0

