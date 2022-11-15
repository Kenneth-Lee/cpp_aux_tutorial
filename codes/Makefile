all: test13-1.o.S test13-1.exe.S

test13-1.o.S: test13-1.o
	objdump -D $< > $@

test13-1.exe.S: test13-1
	objdump -D $< > $@

test13-1.o: test13-1.cpp
	g++ -c $< -o $@

test13-1: test13-1.cpp
	g++ $< -o $@

.PHONY: all clean

clean:
	rm *.o test13-1 *.S
