include ../../config.mk

CFLAGS=-I../../include -Wall -shared -fPIC ${LDFLAGS_LIB} ${LDFLAGS_LINKPATH}..
# XXX
CFLAGS+=-DLIL_ENDIAN=1
CFLAGS+=-L../../util -lr_util -L../../reg -lr_reg -L.. -lr_core
CFLAGS+=-L../../db -lr_db -L../../cons -lr_cons -L../../bin -lr_bin
#CFLAGS+=-L../../anal -lr_anal -L../../core -lr_core
LDFLAGS+=${LINK}

foo: all

ALL_TARGETS=
PLUGS=java.mk

include $(PLUGS)

all: ${ALL_TARGETS}
	@true

clean:
	-rm -f *.${EXT_SO} *.o ${STATIC_OBJ}

mrproper: clean
	-rm -f *.d

.PHONY: all clean foo mrproper
