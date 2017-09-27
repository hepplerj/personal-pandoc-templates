pdfs := $(patsubst %.md,%.md.pdf,$(wildcard *.md))

all: $(pdfs)

%.md.pdf: %.md
	pandoc $< \
		--template=letter-uno.latex \
		-o $@

.PHONY : clean

clean:
	rm $(pdfs)

rebuild: clean all
