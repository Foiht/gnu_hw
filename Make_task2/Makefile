main: start src1.o src2.o src3.o
	gcc main.o src1.o src2.o src3.o -o main

start: main.o
ifeq ($(VAR),by_file)
	@echo "Chosen variant: $(VAR)"
	make -f make1.mk
	make -f make2.mk
	make -f make3.mk
else ifeq ($(VAR),by_include)
	@echo "Chosen variant: $(VAR)"
	include make1.mk
	include make2.mk
	include make3.mk
else
	@echo "Chosen unexpected variant: $(VAR)"
endif

main.o: main.c
	gcc -c main.c

.PHONY:	clean include

clean:
	@rm *.o
	@rm main
