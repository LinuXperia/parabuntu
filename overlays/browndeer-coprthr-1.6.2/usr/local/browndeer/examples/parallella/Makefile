
ifneq (make,)
MAKE = make
endif

EXAMPLES = hello_stdcl clopen_example \
	clvector_example clmulti_array_example 

#	bdt_em3d_e32 bdt_nbody_e32 

##### DO NOT EDIT BELOW THIS LINE #####

SUBDIRS = 
SUBDIRS += $(EXAMPLES)

#export TOPDIR = $(CURDIR)

all: $(SUBDIRS) 

.PHONY: subdirs $(SUBDIRS) clean 

subdirs: $(SUBDIRS)

$(SUBDIRS):
	echo $(MAKECMDGOALS)
	$(MAKE) -C $@ $(MAKECMDGOALS)

clean: subdirs

distclean: subdirs
	@dirs="$(EXAMPLES)"; for dir in $$dirs; do \
	rm -f $$dir/Makefile; \
	done

