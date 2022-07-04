OBJS_C = input.o
OBJS_S = main.o calculate.o error_handling.o
TARGET = clnt serv
cc = gcc
CFLAGS = -g
LDFLAGS = -lkjh

all : $(TARGET)
clnt : $(OBJS_C)
	$(cc) -o $@ input.o

serv : $(OBJS_S)
	ar rscv libkjh.a calculate.o error_handling.o
	$(cc) -o $@ main.o -L. $(LDFLAGS)

input.o : input.c
	$(cc) -c input.c -g

main.o : main.c calc.h
	$(cc) -c main.c -g
calculate.o : calculate.c calc.h
	$(cc) -c calculate.c -g
error_handling.o : error_handling.c calc.h
	$(cc) -c error_handling.c -g

clean :
	rm -f *.o *.a $(TARGET)
