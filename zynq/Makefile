sources := ${wildcard *.scr}

objects := ${sources:%.scr=%.img}

all: $(objects)

$(objects): %.img: %.scr
	mkimage -A arm -T script -C none -n '${basename $<}' -d $< $@
.PHONY:clean
clean:
	rm -f $(objects)
	
