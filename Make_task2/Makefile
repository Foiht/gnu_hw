start:
ifeq ($(VAR),by_file)
	@echo "Chosen variant: $(VAR)"
	make -f make1.mk
	make -f make2.mk
	make -f make3.mk
	make all
else ifeq ($(VAR),by_include)
	@echo "Chosen variant: $(VAR)"
	include make1.mk
	include make2.mk
	include make3.mk
	make all
else
	@echo "Chosen unexpected variant: $(VAR)"
endif

all: main

main: main.o src1.o src2.o src3.o
	gcc $^ -o main

main.o: main.c
	gcc -c main.c

test:
	echo "After test"


.PHONY:	clean

clean:
	@rm *.o
	@rm main
