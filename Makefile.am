
ACLOCAL_AMFLAGS = -I m4

SUBDIRS =

ChangeLog:
	( \
	  echo -e "# created with git log --stat=76 -M -C|fmt -sct -w80\n" ; \
	  git log --stat=76 -M -C|fmt -sct -w80 ; \
	)>$@

AUTHORS.in:
	( \
	  echo "\@PACKAGE\@ -- authors file.  \@DATE\@" ; \
	  echo "" ; \
	  git log|grep '^Author:'|awk '{if(!authors[$$0]){print$$0;authors[$$0]=1;}}'|tac \
	)>$@

README: README.in
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g' $< >$@

NEWS: NEWS.in
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g' $< >$@

AUTHORS: AUTHORS.in
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g' $< >$@

THANKS: THANKS.in
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g' $< >$@

TODO: TODO.in
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g' $< >$@

EXTRA_DIST = autogen.sh configure.template \
	README.in NEWS.in THANKS.in TODO.in

DISTCLEANFILES = AUTHORS AUTHORS.in

nobase_dist_share_DATA =

