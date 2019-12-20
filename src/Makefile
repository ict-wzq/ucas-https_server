TARGET = server
CC = gcc
CFLAGS = -I $(IDIR) 
OBJDIR = obj
IDIR = ../include
LDIR = ../lib
LIBS = -levent -lssl -lcrypto -levent_openssl
_DEPS = ssl_func.h http_func.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))
_OBJ = https_server.o ssl_func.o http_func.o
OBJ = $(patsubst %,$(OBJDIR)/%,$(_OBJ))

$(TARGET) : $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)

$(OBJDIR)/%.o : %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS) $(LIBS)

.PHONY : clean
clean : 
	rm -f $(TARGET) $(OBJDIR)/*.o