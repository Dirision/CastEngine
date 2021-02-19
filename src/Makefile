CC=gcc
IDIR=../include
CFLAGS=-I$(IDIR)

ODIR=../obj
LDIR=../lib

LIBS=-lm

_DEPS = bufferUtils.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))

_OBJ = main.o bufferUtils.o
OBJ=$(patsubst %,$(ODIR)/%,$(_OBJ)) 

$(ODIR)/%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

main: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)

.PHONY: clean
clean: 
	rm -f $(ODIR)/*.o *~ core $(INCDIR)/*~


