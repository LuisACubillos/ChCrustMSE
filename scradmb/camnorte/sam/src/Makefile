EXEC=camnorte

ifdef ComSpec
    RM=del /F /Q
    COPY=copy
else
    RM=rm -rf
    COPY=cp
endif

all: build/debug/base build/release/base clean

build/release/base: build/release $(EXEC).tpl
	@admb -f $(EXEC).tpl
	@$(COPY) $(EXEC) build/release/
	@$(RM) $(EXEC)

build/debug/base: build/debug $(EXEC).tpl
	@admb -g $(EXEC).tpl
	@$(COPY) $(EXEC) build/debug/
	@$(RM) $(EXEC)

build/release:
	@echo creating release directory
	@mkdir -p build/release

build/debug:
	@echo creating debug directory
	@mkdir -p build/debug

clean:
	@$(RM) $(EXEC) *.eva *.log *.rpt *.htp *.cor *.par *.r* *.b* *.p* *.obj
	@$(RM) -f *.rep *.bar *.psv *.std $(EXEC).cpp admodel.* variance *.o *.ecm *.mc2 *.mcm
