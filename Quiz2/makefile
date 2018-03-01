all:	build doczip
	
build: College
	
College: college.o course.o collegemain.o
	g++ college.o course.o collegemain.o -o GPA
	
college.o: college.cc
	g++ -c college.cc
	
course.o: course.cc
	g++ -c course.cc
	
collegemain.o: collegemain.cc
	g++ -c collegemain.cc
	
doczip: collegemain.cc college.cc college.config course.cc college.h course.h node.h tarray.h 2401fal15proj3.doc makefile
	tar -cf archive.tar collegemain.cc college.cc college.config course.cc college.h course.h node.h tarray.h 2401fal15proj3.doc makefile
	
myexe: 
	./GPA	
	
clean:
	rm -f *.o core *.core GPA

doc: 
	doxygen college.config
