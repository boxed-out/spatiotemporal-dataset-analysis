.SUFFIXES:
.SUFFIXES: .rnw .tex .pdf .R


.tex.pdf:; \pdflatex $<; \
	while \grep -q "Rerun to get cross-references right." \
		$(<:.tex=.log); \
	do \
		\pdflatex $<; \
	done 

all: 
	make report.pdf;\
	make neat

pdf: report.pdf

report.pdf: report.tex


neat:
	rm -fr *.core *~ *.aux *.log *.ps *.out *.dvi; 
	rm *.blg *.bbl
	ls

clean:
	rm -fr *.core *~ *.RData *.ps *.pdf *.aux *.log *.out \
		*.bbl *.blg *.toc *.dvi *.eps *.lof \
                *.rel *.ilg *.nlo *.nls *.glo *.gls;
	ls

