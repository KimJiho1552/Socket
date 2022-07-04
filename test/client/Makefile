OBJS = client_main.o client_error.o
TARGET = clnt
cc = gcc
CFLAGS = -g
LDFLAGS = -lclnt

$(TARGET) : $(OBJS)
	ar rscv libclnt.a client_error.o
	$(cc) -o $@ $^ -L. $(LDFLAGS)

.c.o :
	$(cc) $(CFLAGS) -c -o $@ $<

clean :
	rm -f *.o $(TARGET)

client_main.o : client_main.c client.h
client_error.o : client_error.c client.h
