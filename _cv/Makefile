all: cv.pdf

cv.pdf: cv.tex cv.bbl
	pdflatex -interaction=nonstopmode cv.tex

cv.bbl: cv.bcf
	biber cv

cv.bcf: cv.tex
	pdflatex -interaction=nonstopmode cv.tex

cv.tex: template.tex ../_data/* ../scripts/render_from_template.py
	python ../scripts/render_from_template.py template.tex ../_data -o ./cv.tex

.PHONY : clean
clean :
	rm *.log *.aux *.out *.bcf *.bbl *.blg *.log *.run.xml *.stderr *.stdout *.synctex.gz cv.tex
