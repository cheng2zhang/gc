progs=gmc

all: $(progs)

gmc: gmc.c zcom.h
	icc -Wall -Wremarks $< -o $@

remote = cz1@129.109.88.204

Bossman: clean
	rsync -avLz *.[ch] $(remote):/Bossman/cz1/gc

clean:
	find . -name "*~" | xargs rm -f
	rm -rf bin obj a.out $(progs) *.dat
	rstrip.py -Rlv
