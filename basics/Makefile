.PHONY: all
all: basics.pdf

PDFLATEX= 		pdflatex
LATEXFLAGS+= 	-shell-escape
TEX_BBL= 		yes

SRC+=		basics.tex abstract.tex basics.bib
SRC+=		hhcount.sty
FIGURES+= 	collusion.png
FIGURES+= 	password_strength.png password_reuse.png encryptic.png
FIGURES+= 	ltxobj/basics.log.table

basics.pdf: ${SRC} ${FIGURES}

password_strength.png:
	wget -O $@ http://imgs.xkcd.com/comics/password_strength.png

password_reuse.png:
	wget -O $@ http://imgs.xkcd.com/comics/password_reuse.png

encryptic.png:
	wget -O $@ http://imgs.xkcd.com/comics/encryptic.png 

hhcount.sty: hhutils0.sty
hhcount.sty hhutils0.sty:
	wget -O $@ http://tug.ctan.org/tex-archive/usergrps/uktug/baskervi/5_5/$@
	touch $@

ltxobj/basics.log.table: ltxobj/basics.log.gnuplot
	cd $(dir $<) && gnuplot $(notdir $<)

ltxobj/basics.log.gnuplot: ltxobj/basics.aux


.PHONY: clean
clean:
	${RM} basics.pdf


.PHONY: distclean
distclean:
	${RM} password_strength.png
	${RM} password_reuse.png
	${RM} encryptic.png
	${RM} hhcount.sty hhutils0.sty


INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
