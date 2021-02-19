CC=g++
IDIR=../include
CFLAGS=-I$(IDIR)

ODIR=../obj
LDIR=../lib

LIBS=-lm

_DEPS = bufferUtils.h engine.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))

_OBJ = main.o bufferUtils.o engine.o
OBJ=$(patsubst %,$(ODIR)/%,$(_OBJ)) 

$(ODIR)/%.o: %.cpp $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

main: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)

all: main


.PHONY: clean
clean: 
	rm -f $(ODIR)/*.o *~ core $(INCDIR)/*~


