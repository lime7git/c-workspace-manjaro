IDIR 	= ../include
CC	 	= gcc
CFLAGS 	= -I$(IDIR)

ODIR	= ../obj
LDIR	= ../lib

LIBS	= -lm

# header files
_DEPS 	= hellomake.h
DEPS	= $(patsubst %,$(IDIR)/%,$(_DEPS))

# object files
_OBJ 	= hellomake.o hellofun.o
OBJ 	= $(patsubst %,$(ODIR)/%,$(_OBJ))

$(ODIR)/%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

hellomake: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)
	make clean

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o *~ core $(INCDIR)/*~
