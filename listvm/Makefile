objects = listvm.o

listvm : $(objects)
	g++ $< -L.. -lvsphere -o ../list_vm

%.o : %.cpp
	g++ -g -c -I../libvsphere $< -o $@
clean:
	rm -f *.o ../list_vm

.PHONY: clean

