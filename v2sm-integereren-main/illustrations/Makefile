all:	sir.webp

%.pdf:	%.tex
	pdflatex $<
	rm $(basename $<).{aux,log}

%.png:	%.pdf
	convert $< -density 300 -quality 90 $@
	rm $<

%.webp:	%.png
	cwebp $< -o $@
	rm $<
