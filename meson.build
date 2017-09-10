project('libhsakmt', 'c')

# Compiler options
#CFLAGS += -fPIC # Position-independent code required to build shared library
#CFLAGS += -W -Wall -Wextra -Werror -Wno-unused-parameter
#CFLAGS += -Wformat-security -Wswitch-default -Wundef \
#	  -Wshadow -Wpointer-arith -Wbad-function-cast -Wcast-qual \
#	  -Wlogical-op -Wstrict-prototypes -Wmissing-prototypes    \
#	  -Wmissing-declarations -Wredundant-decls                 \
#	  -Wunreachable-code
#CFLAGS += -std=gnu99 -pthread -fvisibility=hidden -O2

# LDFLAGS += -lrt -pthread -lpci -Wl,--version-script=libhsakmt.ver -Wl,-soname=$(LIB_NAME).$(LIB_MAJOR_VER) -Wl,-z,nodelete

# add_global_arguments('-DFOO=bar', language : 'c')

subdir('include')
subdir('src')
subdir('tests')

pkg_mod = import('pkgconfig')
pkg_mod.generate(libraries : hsakmtlib,
                 version : '1.0',
                 name : 'libhsakmt',
                 filebase : 'hsakmt',
                 description : 'AMD Thunk Shitty Library.')
