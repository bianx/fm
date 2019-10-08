PREFIX = $(HOME)
TRG = fm
P = fm_d.pc
SED = sed

install: $P
	mkdir -p -- "$(PREFIX)/share/pkgconfig"
	cp $P "$(PREFIX)/share/pkgconfig"

fm_d.pc: $(TRG).pc.in
	$(SED) "s,@PREFIX@,$(PREFIX),g; s,@PREC@,d,g" $< > $@

clean:; rm -f $P
test:

.PHONY: clean install test
