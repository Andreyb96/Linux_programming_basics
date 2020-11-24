CC = gcc
C_FLAGS = -std=c11
SRC = solution.c
OBJ = $(patsubst %.c,%.o,${SRC})

.PHONY: clean

all: solution

solution: solution.o
	${CC} -o libsolution.so $< -shared

solution.o: ${SRC}
	${CC} -c $< ${C_FLAGS} -fPIC

clean:
	@rm -f *.o *.so *.out
