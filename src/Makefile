# rRootage makefile for Linux

NAME   = rr
O      = o
RM     = rm -f
CC     = gcc
CXX    = g++

PROG   = $(NAME)

DEFAULT_CFLAGS = `sdl-config --cflags`
LDFLAGS        = `sdl-config --libs` -lSDL_mixer -lGL -lGLU -L. -lbulletml -lm

MORE_CFLAGS = -O2 -Wall

CFLAGS   = $(DEFAULT_CFLAGS) $(MORE_CFLAGS)
CXXFLAGS = $(DEFAULT_CFLAGS) $(MORE_CFLAGS) -I./bulletml/

OBJS =	$(NAME).$(O) \
	foe.$(O) foecommand.$(O) barragemanager.$(O) boss.$(O) ship.$(O) laser.$(O) \
	frag.$(O) background.$(O) letterrender.$(O) shot.$(O) \
	screen.$(O) vector.$(O) degutil.$(O) rand.$(O) mt19937int.$(O) \
	soundmanager.$(O) attractmanager.$(O)

$(PROG): $(OBJS) 
	$(CXX) -o $(PROG) $(OBJS) $(LDFLAGS)
	mv $(PROG) ..

clean:
	$(RM) ../$(PROG) *.$(O)