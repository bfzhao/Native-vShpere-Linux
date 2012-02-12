objects = soapC01.o soapC02.o soapC03.o soapC04.o soapC05.o soapC06.o soapC07.o \
	  soapC08.o soapC09.o soapC10.o soapVimBindingProxy.o vim_wrapper.o

libvsphere.so : $(objects)
	g++ *.o -shared -fPIC -lgsoapssl++ -L/usr/lib/i386-linux-gnu -lssl -o ../libvsphere.so

%.o : %.cpp
	g++ -g -c -DWITH_OPENSSL -DWITH_COOKIES $< -o $@

clean:
	rm -f *.o ../libvsphere.so

.PHONY: clean

