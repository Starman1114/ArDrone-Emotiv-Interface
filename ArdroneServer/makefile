CXX           = g++
CXXFLAGS      = -O2 -Wall -D__STDC_CONSTANT_MACROS `pkg-config --libs --cflags opencv`
LIBS          = -lm                     \
                -lpthread               \
                -lavutil                \
                -lavformat              \
                -lavcodec               \
                -lswscale
OBJS          = main.o \
                command.o \
                config.o  \
                udp.o     \
                tcp.o     \
                navdata.o \
                version.o \
                video.o
PROGRAM       = test2.a

$(PROGRAM):     $(OBJS)
	$(CXX) $(OBJS) -o $(PROGRAM) $(CXXFLAGS) $(LDFLAGS) $(LIBS) 

clean:;         rm -f *.o *~ $(PROGRAM) $(OBJS)

install:        $(PROGRAM)
	install -s $(PROGRAM) $(DEST)
