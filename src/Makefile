DIRS = $(filter-out Makefile, $(wildcard *))

all: $(DIRS)

.PHONY: all $(DIRS)
$(DIRS):
	$(MAKE) -C "$@" $(MAKECMDGOALS)
