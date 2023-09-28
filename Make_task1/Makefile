main : 
	gcc -c src1.c src1.h
	gcc -c src2.c src2.h
	gcc -c src3.c src3.h
	gcc -c main.c src1.h src2.h src3.h
	gcc src1.o src2.o src3.o main.o -o main

clean:
	@rm *.o
	@rm *.gch
	@rm main
