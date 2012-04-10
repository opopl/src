PROG =	cff

SRCS =	cff.f90

OBJS =	cff.o

LIBS =	

CC = cc
CFLAGS = -O
FC = $(FC90)
FFLAGS = -O
F90 = $(FC90)
F90FLAGS = -O
LDFLAGS = -s

all: cff.f90 $(PROG)

cff.f90: cff.sh
	$^ > $@

$(PROG): $(OBJS)
	$(F90) $(LDFLAGS) -o $@ $(OBJS) $(LIBS)

clean:
	rm -f $(PROG) $(OBJS) *.mod

.SUFFIXES: $(SUFFIXES) .f90

.f90.o:
	$(F90) $(F90FLAGS) -c $<

