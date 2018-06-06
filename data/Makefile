CSVS := $(wildcard *.csv)
GZS := $(patsubst %.csv,%.tar.gz,$(CSVS))

all: $(GZS) md5-csv.txt md5-gz.txt

%.tar.gz: %.csv
	GZIP=-9 tar czvf $@ $^

md5-csv.txt: $(CSVS)
	md5sum *.csv > $@

md5-gz.txt: $(GZS)
	md5sum *.gz > $@

