CSVS := $(wildcard *.csv)
GZS := $(patsubst %.csv,%.tar.gz,$(CSVS))

all: $(GZS)

%.tar.gz: %.csv
	GZIP=-9 tar czvf $@ $^

