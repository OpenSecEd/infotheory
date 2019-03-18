.PHONY: all
all: applications.pdf

SRC+=		applications.tex preamble.tex applications.bib
SRC+= 		abstract.tex contents.tex
SRC+=		hhcount.sty
FIGURES+= 	collusion.png
FIGURES+= 	password_strength.png password_reuse.png encryptic.png

applications.pdf: ${SRC} ${FIGURES}

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


.PHONY: clean
clean:
	${RM} applications.pdf
	${RM} applications.bbl applications.log.gnuplot applications.log.table applications.nav applications.run.xml applications.snm applications.vrb


.PHONY: distclean
distclean:
	${RM} password_strength.png
	${RM} password_reuse.png
	${RM} encryptic.png
	${RM} hhcount.sty hhutils0.sty


INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
