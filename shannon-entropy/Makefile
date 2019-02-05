.PHONY: all
all: shannon-entropy.pdf

LATEXFLAGS+= 	-shell-escape
TEX_OUTDIR= 	.

SRC+=		shannon-entropy.tex preamble.tex shannon-entropy.bib
SRC+= 		abstract.tex contents.tex
SRC+=		hhcount.sty

shannon-entropy.pdf: ${SRC}

hhcount.sty: hhutils0.sty
hhcount.sty hhutils0.sty:
	wget -O $@ http://tug.ctan.org/tex-archive/usergrps/uktug/baskervi/5_5/$@
	touch $@


.PHONY: clean
clean:
	${RM} shannon-entropy.pdf
	${RM} shannon-entropy.bbl shannon-entropy.log.gnuplot shannon-entropy.log.table shannon-entropy.nav shannon-entropy.run.xml shannon-entropy.snm shannon-entropy.vrb


.PHONY: distclean
distclean:
	${RM} password_strength.png
	${RM} password_reuse.png
	${RM} encryptic.png
	${RM} hhcount.sty hhutils0.sty


INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
