.PHONY: all clean

all: morphological-analyser.hfst

lexicon.hfst: root.lexc nouns.lexc
	hfst-lexc $^ -o $@

%.hfst: %.twolc
	hfst-twolc -i $< -o $@ --resolve

morphological-analyser.hfst: lexicon.hfst morphographemics.hfst
	hfst-compose-intersect lexicon.hfst morphographemics.hfst -o $@

clean:
	-rm -f *.hfst
