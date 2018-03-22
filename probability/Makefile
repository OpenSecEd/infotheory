.PHONY: all
all: slides.pdf

SRC+=		preamble.tex
SRC+=		abstract.tex contents.tex
DEPENDS+=	hhcount.sty

slides.pdf: slides.tex
slides.pdf: ${SRC} ${DEPENDS}


hhcount.sty: hhutils0.sty
hhcount.sty hhutils0.sty:
	wget -O $@ http://tug.ctan.org/tex-archive/usergrps/uktug/baskervi/5_5/$@
	touch $@


.PHONY: clean
clean:
	${RM} slides.pdf


.PHONY: distclean clean-depends
distclean clean-depends:
	${RM} hhcount.sty hhutils0.sty


INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
