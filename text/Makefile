
objects := $(patsubst %.text,%.meta,$(wildcard *.text))

%.meta: %.text
	awk "BEGIN { text=0; } text<=1 {print} /^---$$/ { text = text + 1; }" $< > $@

default: $(objects)

.PHONY : clean
clean:
	rm *.meta
