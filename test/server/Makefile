OBJS = server_main.o server_calculate.o server_error.o
TARGET = serv
cc = gcc
CFLAGS = -g
LDFLAGS = -lserv

$(TARGET) : $(OBJS)
	$(cc) -o $@ $^ -L. $(LDFLAGS)

.c.o :
	$(cc) $(CFLAGS) -c -o $@ $<

clean :
	rm -f *.o $(TARGET)

server_main.o : server_main.c server.h
server_calculate.o : server_calculate.c server.h
server_error.o : server_error.c server.h
