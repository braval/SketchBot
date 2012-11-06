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
WS_ROOT_DIR := Z:/RTES/workspace
PRJ_ROOT_DIR := $(WS_ROOT_DIR)/project



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
PROJECT_TARGETS = project/$(MODE_DIR)/project.out \
	 project_partialImage/$(MODE_DIR)/project_partialImage.o


#Rules

# project
ifeq ($(DEBUG_MODE),1)
project/$(MODE_DIR)/% : DEBUGFLAGS_C-Compiler = -g
project/$(MODE_DIR)/% : DEBUGFLAGS_C++-Compiler = -g
project/$(MODE_DIR)/% : DEBUGFLAGS_Linker = -g
project/$(MODE_DIR)/% : DEBUGFLAGS_Partial-Image-Linker = 
project/$(MODE_DIR)/% : DEBUGFLAGS_Librarian = 
project/$(MODE_DIR)/% : DEBUGFLAGS_Assembler = -g
else
project/$(MODE_DIR)/% : DEBUGFLAGS_C-Compiler = -O2
project/$(MODE_DIR)/% : DEBUGFLAGS_C++-Compiler = -O2
project/$(MODE_DIR)/% : DEBUGFLAGS_Linker = -O2
project/$(MODE_DIR)/% : DEBUGFLAGS_Partial-Image-Linker = 
project/$(MODE_DIR)/% : DEBUGFLAGS_Librarian = 
project/$(MODE_DIR)/% : DEBUGFLAGS_Assembler = -O2
endif
project/$(MODE_DIR)/% : IDE_INCLUDES = -I$(WIND_BASE)/target/h -I$(WIND_BASE)/target/h/wrn/coreip 
project/$(MODE_DIR)/% : IDE_LIBRARIES = 
project/$(MODE_DIR)/% : PROJECT_TYPE = DKM
project/$(MODE_DIR)/% : DEFINES = 
project/$(MODE_DIR)/% : EXPAND_DBG = 0
project/$(MODE_DIR)/% : VX_CPU_FAMILY = pentium
project/$(MODE_DIR)/% : CPU = PENTIUM4
project/$(MODE_DIR)/% : TOOL_FAMILY = gnu
project/$(MODE_DIR)/% : TOOL = gnu
project/$(MODE_DIR)/% : TOOL_PATH = 
project/$(MODE_DIR)/% : CC_ARCH_SPEC = -mtune=pentium4 -march=pentium4 -nostdlib -fno-builtin -fno-defer-pop
project/$(MODE_DIR)/% : VSB_DIR = $(WIND_BASE)/target/lib
project/$(MODE_DIR)/% : VSB_CONFIG_FILE = $(VSB_DIR)/h/config/vsbConfig.h
project/$(MODE_DIR)/% : LIBPATH = 
project/$(MODE_DIR)/% : LIBS = 
project/$(MODE_DIR)/% : OBJ_DIR := project/$(MODE_DIR)

OBJECTS_project = project_partialImage/$(MODE_DIR)/project_partialImage.o

project/$(MODE_DIR)/project.out : $(OBJECTS_project)
	$(TRACE_FLAG)if [ ! -d "`dirname "$@"`" ]; then mkdir -p "`dirname "$@"`"; fi;echo "building $@";rm -f "$@";nmpentium $(OBJECTS_project) $(IDE_LIBRARIES) | tclsh $(WIND_BASE)/host/resource/hutils/tcl/munch.tcl -c pentium -tags $(VSB_DIR)/tags/pentium/PENTIUM4/common/dkm.tags > $(OBJ_DIR)/ctdt.c; $(TOOL_PATH)ccpentium $(DEBUGFLAGS_Linker) $(CC_ARCH_SPEC) -fdollars-in-identifiers -Wall  $(ADDED_CFLAGS) $(IDE_INCLUDES) $(ADDED_INCLUDES) -DCPU=$(CPU) -DTOOL_FAMILY=$(TOOL_FAMILY) -DTOOL=$(TOOL) -D_WRS_KERNEL  -D_VSB_CONFIG_FILE=\"$(VSB_CONFIG_FILE)\"   $(DEFINES)  -o $(OBJ_DIR)/ctdt.o -c $(OBJ_DIR)/ctdt.c; $(TOOL_PATH)ccpentium -r -nostdlib -Wl,-X -T $(WIND_BASE)/target/h/tool/gnu/ldscripts/link.OUT -o "$@" $(OBJ_DIR)/ctdt.o $(OBJECTS_project) $(IDE_LIBRARIES) $(LIBPATH) $(LIBS) $(ADDED_LIBPATH) $(ADDED_LIBS) && if [ "$(EXPAND_DBG)" = "1" ]; then plink "$@";fi

project/$(MODE_DIR)/project_compile_file : $(FILE) ;

_clean :: project/$(MODE_DIR)/project_clean

project/$(MODE_DIR)/project_clean : 
	$(TRACE_FLAG)if [ -d "project" ]; then cd "project"; rm -rf $(MODE_DIR); fi


# project_partialImage
ifeq ($(DEBUG_MODE),1)
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_C-Compiler = -g
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_C++-Compiler = -g
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Linker = -g
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Partial-Image-Linker = 
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Librarian = 
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Assembler = -g
else
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_C-Compiler = -O2
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_C++-Compiler = -O2
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Linker = -O2
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Partial-Image-Linker = 
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Librarian = 
project_partialImage/$(MODE_DIR)/% : DEBUGFLAGS_Assembler = -O2
endif
project_partialImage/$(MODE_DIR)/% : IDE_INCLUDES = -I$(WIND_BASE)/target/h -I$(WIND_BASE)/target/h/wrn/coreip 
project_partialImage/$(MODE_DIR)/% : IDE_LIBRARIES = 
project_partialImage/$(MODE_DIR)/% : PROJECT_TYPE = DKM
project_partialImage/$(MODE_DIR)/% : DEFINES = 
project_partialImage/$(MODE_DIR)/% : EXPAND_DBG = 0
project_partialImage/$(MODE_DIR)/% : VX_CPU_FAMILY = pentium
project_partialImage/$(MODE_DIR)/% : CPU = PENTIUM4
project_partialImage/$(MODE_DIR)/% : TOOL_FAMILY = gnu
project_partialImage/$(MODE_DIR)/% : TOOL = gnu
project_partialImage/$(MODE_DIR)/% : TOOL_PATH = 
project_partialImage/$(MODE_DIR)/% : CC_ARCH_SPEC = -mtune=pentium4 -march=pentium4 -nostdlib -fno-builtin -fno-defer-pop
project_partialImage/$(MODE_DIR)/% : VSB_DIR = $(WIND_BASE)/target/lib
project_partialImage/$(MODE_DIR)/% : VSB_CONFIG_FILE = $(VSB_DIR)/h/config/vsbConfig.h
project_partialImage/$(MODE_DIR)/% : LIBPATH = 
project_partialImage/$(MODE_DIR)/% : LIBS = 
project_partialImage/$(MODE_DIR)/% : OBJ_DIR := project_partialImage/$(MODE_DIR)

project_partialImage/$(MODE_DIR)/Objects/project/btvid3.o : $(PRJ_ROOT_DIR)/btvid3.c
	$(TRACE_FLAG)if [ ! -d "`dirname "$@"`" ]; then mkdir -p "`dirname "$@"`"; fi;echo "building $@"; $(TOOL_PATH)ccpentium $(DEBUGFLAGS_C-Compiler) $(CC_ARCH_SPEC) -ansi  -Wall   -MD -MP $(ADDED_CFLAGS) $(IDE_INCLUDES) $(ADDED_INCLUDES) -DCPU=$(CPU) -DTOOL_FAMILY=$(TOOL_FAMILY) -DTOOL=$(TOOL) -D_WRS_KERNEL  -D_VSB_CONFIG_FILE=\"$(VSB_CONFIG_FILE)\"   $(DEFINES) -o "$@" -c "$<"


OBJECTS_project_partialImage = project_partialImage/$(MODE_DIR)/Objects/project/btvid3.o

project_partialImage/$(MODE_DIR)/project_partialImage.o : $(OBJECTS_project_partialImage)
	$(TRACE_FLAG)if [ ! -d "`dirname "$@"`" ]; then mkdir -p "`dirname "$@"`"; fi;echo "building $@"; $(TOOL_PATH)ccpentium -r -nostdlib -Wl,-X  -o "$@" $(OBJECTS_project_partialImage) $(ADDED_OBJECTS) $(IDE_LIBRARIES) $(LIBPATH) $(LIBS) $(ADDED_LIBPATH) $(ADDED_LIBS) && if [ "$(EXPAND_DBG)" = "1" ]; then plink "$@";fi

project_partialImage/$(MODE_DIR)/project_partialImage_compile_file : $(FILE) ;

_clean :: project_partialImage/$(MODE_DIR)/project_partialImage_clean

project_partialImage/$(MODE_DIR)/project_partialImage_clean : 
	$(TRACE_FLAG)if [ -d "project_partialImage" ]; then cd "project_partialImage"; rm -rf $(MODE_DIR); fi

DEP_FILES := project_partialImage/$(MODE_DIR)/Objects/project/btvid3.d
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
