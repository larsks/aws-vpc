TEFILES=$(wildcard *.te)
PPFILES=$(TEFILES:.te=.pp)

%.pp: %.te
	make -f /usr/share/selinux/devel/Makefile $@

all: $(PPFILES)

install: all
	for module in $(PPFILES); do semodule -i $$module; done

