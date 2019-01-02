IDIR=../include
QTI=/usr/include/x86_64-linux-gnu/qt5
CXX=g++
CXXFLAGS=-I$(IDIR) -I$(QTI) -fPIC -std=c++1z

ODIR=obj
LDIR =../lib

LIBS=-lQt5Core -lQt5Gui

_DEPS = cpp_file.h logging.h options.h replaces.h generator.h data.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))

_OBJ = cpp_file.o logging.o options.o replaces.o generator.o data.o main.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))


$(ODIR)/%.o: %.cpp $(DEPS)
	$(CXX) -c -o $@ $< $(CXXFLAGS)

emoji_codegen: $(OBJ)
	$(CXX) -o $@ $^ $(CXXFLAGS) -L/usr/lib/x86_64-linux-gnu/ $(LIBS)

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o *~ core $(INCDIR)/*~ 
