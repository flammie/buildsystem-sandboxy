## Process this file with automake to produce Makefile.in

LEXC_SRCS=root.lexc nouns.lexc
TWOLC_SRCS=morphographemics.twolc
EXTRA_DIST=$(LEXC_SRCS) $(TWOLC_SRCS)

hfstdatadir=$(pkgdatadir)
hfstdata_DATA=morphological-analyser.hfst

lexicon.hfst: $(LEXC_SRCS)
	$(HFST_LEXC) $^ -o $@

%.hfst: %.twolc
	$(HFST_TWOLC) -i $< -o $@ --resolve

morphological-analyser.hfst: lexicon.hfst morphographemics.hfst
	$(HFST_COMPOSE_INTERSECT) lexicon.hfst morphographemics.hfst -o $@

clean-local:
	-rm -f *.hfst
