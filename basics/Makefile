.PHONY: all
all: basics.pdf

LATEXFLAGS+=	-shell-escape

SRC+=		basics.tex abstract.tex basics.bib
SRC+=		hhcount.sty
FIGURES+= 	collusion.png
FIGURES+= 	password_strength.png password_reuse.png encryptic.png

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


.PHONY: clean-depends
clean-depends:
	${RM} password_strength.png
	${RM} password_reuse.png
	${RM} encryptic.png
	${RM} hhcount.sty hhutils0.sty


INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
