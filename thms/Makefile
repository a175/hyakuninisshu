LATEX=platex
#LATEX=pdflatex
BIBTEX=bibtex
DVI2PDF=dvipdfmx
TEXFILE=x2
MAINTEXFILES=p.tex

all: pdf
dvi: ${TEXFILE}.dvi
pdf: ${TEXFILE}.pdf

${TEXFILE}.dvi: ${TEXFILE}.tex 
	${LATEX} ${TEXFILE} && ${LATEX} ${TEXFILE}
${TEXFILE}.pdf: ${TEXFILE}.dvi
	${DVI2PDF} ${TEXFILE}.dvi

#${TEXFILE}.pdf: ${TEXFILE}.tex ${MAINTEXFILE}.tex ${TEXFILE}.bbl
#${TEXFILE}.pdf: ${TEXFILE}.tex ${MAINTEXFILE}.tex 
#	${LATEX} ${TEXFILE} && ${LATEX} ${TEXFILE} && ${LATEX} ${TEXFILE}
#${TEXFILE}.bbl: ${TEXFILE}.tex by-mr.bib

#bbl: ${TEXFILE}.bbl
#bbl:
#	${LATEX} ${TEXFILE} && ${BIBTEX} ${TEXFILE}

view:
	evince ${TEXFILE}.pdf &
clean:
	rm -f ${TEXFILE}.dvi ${TEXFILE}.pdf ${TEXFILE}.log ${TEXFILE}.aux texput.log ${TEXFILE}.out ${TEXFILE}.bbl ${TEXFILE}.blg
