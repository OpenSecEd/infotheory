.PHONY: all
all: slides.pdf

SRC+=		preamble.tex
SRC+=		abstract.tex contents.tex

DEPENDS+= 	bibsp.sty

LATEXFLAGS+= 	-shell-escape
TEX_OUTDIR= 	.

slides.pdf: slides.tex
slides.pdf: ${SRC} ${DEPENDS}


.PHONY: clean
clean:
	${RM} slides.pdf


INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
INCLUDE_BIBSP=../bibsp
include ${INCLUDE_BIBSP}/bibsp.mk
