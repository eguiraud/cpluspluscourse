all: C++Course.pdf

essentials:
	ESSENTIALS=1 make

%.pdf: *.tex **/*.tex
ifdef ESSENTIALS
	echo "\basictrue" > onlybasics.tex
else
	rm -f onlybasics.tex
endif
	pdflatex -shell-escape C++Course.tex
	pdflatex -shell-escape C++Course.tex

clean:
	rm -rf *.aux */*.aux *.log *.nav *.out *.pyg *.snm *.vrb *.toc C++Course.l* _minted-C++Course

clobber: clean
	rm -f C++Course.pdf
