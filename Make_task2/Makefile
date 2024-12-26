ifdef USE_INCLUDE
    include make1.mk make2.mk make3.mk
else
    submakes:
	    make -f make1.mk
	    make -f make2.mk
	    make -f make3.mk
endif

all: main.c  src1.o src2.o src3.o
	gcc $^ -o build-all

main.o: main.c
	$(CC) -c main.c

clean:
	rm -f *.o build-all

.PHONY: clean submakes

