#Makefile for building and running the camaron model
EXEC = camnorte
DIST = ../src/
TPL  = $(EXEC).tpl
ARGS = -nox -iprint 50 -ind $(EXEC).dat

# use 1 to use release admb version
ifeq ($(type),1)
	MOD = build/release/
else
	MOD = build/debug/
endif

all: run clean
# compile source code if *.tpl changed
$(EXEC): $(DIST)$(TPL)
	$(MAKE) --directory=../src

# run model with arguments
run: $(EXEC)
	echo "---------------------------------"
	echo "Copying model from "$(MOD)
	echo "---------------------------------"
	cp $(DIST)$(MOD)$(EXEC) base
	./base $(ARGS)
	@mkdir -p results
	cp base.rep results/$(EXEC).rep
	cp base.par results/$(EXEC).par
	cp base.bar results/$(EXEC).bar
	cp base.std results/$(EXEC).std
	cp base.cor results/$(EXEC).cor
  # R CMD BATCH camaron_plots.R

clean:
	rm -f $(EXEC)
	rm -f *.eva *.log *.rpt *.htp *.cor *.par *.r* *.b* *.p* proj.dat mceval.dat Fprof.yld
	rm -f *.csv *.rep *.bar *.psv *.std $(EXEC).cpp admodel.* variance *.o *.ecm *.mc2 *.mcm
