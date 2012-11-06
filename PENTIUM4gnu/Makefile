# Wind River Workbench generated Makefile.
# Do not edit!!!
#
# The file ".wrmakefile" is the template used by the Wind River Workbench to
# generate the makefiles of this project. Add user-specific build targets and
# make rules only(!) in this project's ".wrmakefile" file. These will then be
# automatically dumped into the makefiles.

WIND_HOME := $(subst \,/,$(WIND_HOME))
WIND_BASE := $(subst \,/,$(WIND_BASE))
WIND_USR := $(subst \,/,$(WIND_USR))
WRVX_COMPBASE := $(subst \,/,$(WRVX_COMPBASE))

all : pre_build main_all post_build

_clean ::
	@echo "make: removing targets and objects of `pwd`"

TRACE=0
TRACEON=$(TRACE:0=@)
TRACE_FLAG=$(TRACEON:1=)

MAKEFILE := Makefile

FLEXIBLE_BUILD := 1

BUILD_SPEC = PENTIUM4gnu
DEBUG_MODE = 1
ifeq ($(DEBUG_MODE),1)
MODE_DIR := Debug
else
MODE_DIR := NonDebug
endif
OBJ_DIR := .
WS_ROOT_DIR := C:/
PRJ_ROOT_DIR := $(WS_ROOT_DIR)//SketchBot



#Global Build Macros
PROJECT_TYPE = DKM
DEFINES = 
EXPAND_DBG = 0


#BuildSpec specific Build Macros
VX_CPU_FAMILY = pentium
CPU = PENTIUM4
TOOL_FAMILY = gnu
TOOL = gnu
TOOL_PATH = 
CC_ARCH_SPEC = -mtune=pentium4 -march=pentium4 -nostdlib -fno-builtin -fno-defer-pop
VSB_DIR = $(WIND_BASE)/target/lib
VSB_CONFIG_FILE = $(VSB_DIR)/h/config/vsbConfig.h
LIBPATH = 
LIBS = 

IDE_INCLUDES = -I$(WIND_BASE)/target/h -I$(WIND_BASE)/target/h/wrn/coreip 

IDE_LIBRARIES = 



#BuildTool flags
ifeq ($(DEBUG_MODE),1)
DEBUGFLAGS_C-Compiler = -g
DEBUGFLAGS_C++-Compiler = -g
DEBUGFLAGS_Linker = -g
DEBUGFLAGS_Partial-Image-Linker = 
DEBUGFLAGS_Librarian = 
DEBUGFLAGS_Assembler = -g
else
DEBUGFLAGS_C-Compiler = -O2
DEBUGFLAGS_C++-Compiler = -O2
DEBUGFLAGS_Linker = -O2
DEBUGFLAGS_Partial-Image-Linker = 
DEBUGFLAGS_Librarian = 
DEBUGFLAGS_Assembler = -O2
endif


#Project Targets
PROJECT_TARGETS = SketchBot/$(MODE_DIR)/SketchBot.out \
	 SketchBot_partialImage/$(MODE_DIR)/SketchBot_partialImage.o


#Rules

# SketchBot
ifeq ($(DEBUG_MODE),1)
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_C-Compiler = -g
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_C++-Compiler = -g
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_Linker = -g
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_Partial-Image-Linker = 
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_Librarian = 
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_Assembler = -g
else
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_C-Compiler = -O2
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_C++-Compiler = -O2
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_Linker = -O2
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_Partial-Image-Linker = 
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_Librarian = 
SketchBot/$(MODE_DIR)/% : DEBUGFLAGS_Assembler = -O2
endif
SketchBot/$(MODE_DIR)/% : IDE_INCLUDES = -I$(WIND_BASE)/target/h -I$(WIND_BASE)/target/h/wrn/coreip 
SketchBot/$(MODE_DIR)/% : IDE_LIBRARIES = 
SketchBot/$(MODE_DIR)/% : PROJECT_TYPE = DKM
SketchBot/$(MODE_DIR)/% : DEFINES = 
SketchBot/$(MODE_DIR)/% : EXPAND_DBG = 0
SketchBot/$(MODE_DIR)/% : VX_CPU_FAMILY = pentium
SketchBot/$(MODE_DIR)/% : CPU = PENTIUM4
SketchBot/$(MODE_DIR)/% : TOOL_FAMILY = gnu
SketchBot/$(MODE_DIR)/% : TOOL = gnu
SketchBot/$(MODE_DIR)/% : TOOL_PATH = 
SketchBot/$(MODE_DIR)/% : CC_ARCH_SPEC = -mtune=pentium4 -march=pentium4 -nostdlib -fno-builtin -fno-defer-pop
SketchBot/$(MODE_DIR)/% : VSB_DIR = $(WIND_BASE)/target/lib
SketchBot/$(MODE_DIR)/% : VSB_CONFIG_FILE = $(VSB_DIR)/h/config/vsbConfig.h
SketchBot/$(MODE_DIR)/% : LIBPATH = 
SketchBot/$(MODE_DIR)/% : LIBS = 
SketchBot/$(MODE_DIR)/% : OBJ_DIR := SketchBot/$(MODE_DIR)

OBJECTS_SketchBot = SketchBot_partialImage/$(MODE_DIR)/SketchBot_partialImage.o

SketchBot/$(MODE_DIR)/SketchBot.out : $(OBJECTS_SketchBot)
	$(TRACE_FLAG)if [ ! -d "`dirname "$@"`" ]; then mkdir -p "`dirname "$@"`"; fi;echo "building $@";rm -f "$@";nmpentium $(OBJECTS_SketchBot) $(IDE_LIBRARIES) | tclsh $(WIND_BASE)/host/resource/hutils/tcl/munch.tcl -c pentium -tags $(VSB_DIR)/tags/pentium/PENTIUM4/common/dkm.tags > $(OBJ_DIR)/ctdt.c; $(TOOL_PATH)ccpentium $(DEBUGFLAGS_Linker) $(CC_ARCH_SPEC) -fdollars-in-identifiers -Wall  $(ADDED_CFLAGS) $(IDE_INCLUDES) $(ADDED_INCLUDES) -DCPU=$(CPU) -DTOOL_FAMILY=$(TOOL_FAMILY) -DTOOL=$(TOOL) -D_WRS_KERNEL  -D_VSB_CONFIG_FILE=\"$(VSB_CONFIG_FILE)\"   $(DEFINES)  -o $(OBJ_DIR)/ctdt.o -c $(OBJ_DIR)/ctdt.c; $(TOOL_PATH)ccpentium -r -nostdlib -Wl,-X -T $(WIND_BASE)/target/h/tool/gnu/ldscripts/link.OUT -o "$@" $(OBJ_DIR)/ctdt.o $(OBJECTS_SketchBot) $(IDE_LIBRARIES) $(LIBPATH) $(LIBS) $(ADDED_LIBPATH) $(ADDED_LIBS) && if [ "$(EXPAND_DBG)" = "1" ]; then plink "$@";fi

SketchBot/$(MODE_DIR)/SketchBot_compile_file : $(FILE) ;

_clean :: SketchBot/$(MODE_DIR)/SketchBot_clean

SketchBot/$(MODE_DIR)/SketchBot_clean : 
	$(TRACE_FLAG)if [ -d "SketchBot" ]; then cd "SketchBot"; rm -rf $(MODE_DIR); fi


# SketchBot_partialImage
ifeq ($(DEBUG_MODE),1)
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_C-Compiler = -g
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_C++-Compiler = -g
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Linker = -g
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Partial-Image-Linker = 
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Librarian = 
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Assembler = -g
else
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_C-Compiler = -O2
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_C++-Compiler = -O2
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Linker = -O2
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Partial-Image-Linker = 
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Librarian = 
SketchBot_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Assembler = -O2
endif
SketchBot_partialImage/$(MODE_DIR)/% : IDE_INCLUDES = -I$(WIND_BASE)/target/h -I$(WIND_BASE)/target/h/wrn/coreip 
SketchBot_partialImage/$(MODE_DIR)/% : IDE_LIBRARIES = 
SketchBot_partialImage/$(MODE_DIR)/% : PROJECT_TYPE = DKM
SketchBot_partialImage/$(MODE_DIR)/% : DEFINES = 
SketchBot_partialImage/$(MODE_DIR)/% : EXPAND_DBG = 0
SketchBot_partialImage/$(MODE_DIR)/% : VX_CPU_FAMILY = pentium
SketchBot_partialImage/$(MODE_DIR)/% : CPU = PENTIUM4
SketchBot_partialImage/$(MODE_DIR)/% : TOOL_FAMILY = gnu
SketchBot_partialImage/$(MODE_DIR)/% : TOOL = gnu
SketchBot_partialImage/$(MODE_DIR)/% : TOOL_PATH = 
SketchBot_partialImage/$(MODE_DIR)/% : CC_ARCH_SPEC = -mtune=pentium4 -march=pentium4 -nostdlib -fno-builtin -fno-defer-pop
SketchBot_partialImage/$(MODE_DIR)/% : VSB_DIR = $(WIND_BASE)/target/lib
SketchBot_partialImage/$(MODE_DIR)/% : VSB_CONFIG_FILE = $(VSB_DIR)/h/config/vsbConfig.h
SketchBot_partialImage/$(MODE_DIR)/% : LIBPATH = 
SketchBot_partialImage/$(MODE_DIR)/% : LIBS = 
SketchBot_partialImage/$(MODE_DIR)/% : OBJ_DIR := SketchBot_partialImage/$(MODE_DIR)

SketchBot_partialImage/$(MODE_DIR)/Objects/SketchBot/btvid3.o : $(PRJ_ROOT_DIR)/btvid3.c
	$(TRACE_FLAG)if [ ! -d "`dirname "$@"`" ]; then mkdir -p "`dirname "$@"`"; fi;echo "building $@"; $(TOOL_PATH)ccpentium $(DEBUGFLAGS_C-Compiler) $(CC_ARCH_SPEC) -ansi  -Wall   -MD -MP $(ADDED_CFLAGS) $(IDE_INCLUDES) $(ADDED_INCLUDES) -DCPU=$(CPU) -DTOOL_FAMILY=$(TOOL_FAMILY) -DTOOL=$(TOOL) -D_WRS_KERNEL  -D_VSB_CONFIG_FILE=\"$(VSB_CONFIG_FILE)\"   $(DEFINES) -o "$@" -c "$<"


OBJECTS_SketchBot_partialImage = SketchBot_partialImage/$(MODE_DIR)/Objects/SketchBot/btvid3.o

SketchBot_partialImage/$(MODE_DIR)/SketchBot_partialImage.o : $(OBJECTS_SketchBot_partialImage)
	$(TRACE_FLAG)if [ ! -d "`dirname "$@"`" ]; then mkdir -p "`dirname "$@"`"; fi;echo "building $@"; $(TOOL_PATH)ccpentium -r -nostdlib -Wl,-X  -o "$@" $(OBJECTS_SketchBot_partialImage) $(ADDED_OBJECTS) $(IDE_LIBRARIES) $(LIBPATH) $(LIBS) $(ADDED_LIBPATH) $(ADDED_LIBS) && if [ "$(EXPAND_DBG)" = "1" ]; then plink "$@";fi

SketchBot_partialImage/$(MODE_DIR)/SketchBot_partialImage_compile_file : $(FILE) ;

_clean :: SketchBot_partialImage/$(MODE_DIR)/SketchBot_partialImage_clean

SketchBot_partialImage/$(MODE_DIR)/SketchBot_partialImage_clean : 
	$(TRACE_FLAG)if [ -d "SketchBot_partialImage" ]; then cd "SketchBot_partialImage"; rm -rf $(MODE_DIR); fi

DEP_FILES := SketchBot_partialImage/$(MODE_DIR)/Objects/SketchBot/btvid3.d
-include $(DEP_FILES)


WIND_SCOPETOOLS_BASE := $(subst \,/,$(WIND_SCOPETOOLS_BASE))

clean_scopetools :
	$(TRACE_FLAG)rm -rf $(PRJ_ROOT_DIR)/.coveragescope/db

CLEAN_STEP := clean_scopetools


-include $(PRJ_ROOT_DIR)/*.makefile

-include *.makefile

JOBS?=1
ifeq ($(JOBS),1)
main_all : external_build  $(PROJECT_TARGETS)
	@echo "make: built targets of `pwd`"
else
main_all : external_build 
	@$(MAKE) -f $(MAKEFILE) --jobs $(JOBS) $(MFLAGS) $(PROJECT_TARGETS);\
	echo "make: built targets of `pwd`"
endif 

# entry point for extending the build
external_build ::
	@echo ""

# main entry point for pre processing prior to the build
pre_build :: $(PRE_BUILD_STEP) generate_sources
	@echo ""

# entry point for generating sources prior to the build
generate_sources ::
	@echo ""

# main entry point for post processing after the build
post_build :: $(POST_BUILD_STEP) deploy_output
	@echo ""

# entry point for deploying output after the build
deploy_output ::
	@echo ""

clean :: external_clean $(CLEAN_STEP) _clean

# entry point for extending the build clean
external_clean ::
	@echo ""
