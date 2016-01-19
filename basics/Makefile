.PHONY: all
all: basics.pdf

SRC=		basics.tex abstract.tex basics.bib
FIGURES= 	collusion.png
FIGURES+= 	password_strength.png password_reuse.png encryptic.png

infotheory.pdf: ${SRC} ${FIGURES}

password_strength.png:
	wget -O $@ http://imgs.xkcd.com/comics/password_strength.png

password_reuse.png:
	wget -O $@ http://imgs.xkcd.com/comics/password_reuse.png

encryptic.png:
	wget -O $@ http://imgs.xkcd.com/comics/encryptic.png 


.PHONY: clean-depends
clean-depends:
	${RM} password_strength.png
	${RM} password_reuse.png
	${RM} encryptic.png


INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
