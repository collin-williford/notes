 - Example: a person has multiple attributes 
	 - Name
	 - weight
	 - height
	 - gender
	 - id number
	 - age
 - To indicate these are all parts of the same entity, we define a struct data type for persons

Declaring Structs
 - struct {
	 - char name\[len];
	 - int height;
	 - int weight
	 - char gender;
	 - int indnum'
	 - short age;
	 - }

Structs in Memory 
 - struct members stored in memory in order delcared
 - Each member is allocated the amout of memory approopriate to its type 
 - Members are in the same memory block
	 - There my be offsets

struct Name Space
 - A struct is a new scope 
 - Two different structs can have members with the same names

Initializing Named structs
 - Unitialized
	 - struct person person1;
- Fully initialized
	- struct person person1 = {"Fred", 72, 180, "M", 12345, 20};
- Partially initialized (part 1)
	- struct person person1 = {"Fred", 72, 180, "m"}
- Partially Initialized (part 2)
	- struct person person1 = {.name = "Fred", .height = 72, .gender = "M", .idnum = 12345};

Referring to structs and memebers
 - simple assigmenet to a struct member
	 - person3.weight = 200;
- Assignement to an entire struct (version 1)
	- person2 - person1;
- Assignemtn to an entire struct (version 2)
	- person4 = (struct person) {"Mary", 66, 125, 'F', 98765, 21};

structs can contain structs
 - One struct
	 - struct date {
		   usisigned short month;
		   unsigned short doay;
		   unsigned int year;
		}
 - Contained in another struct
	 - struct person-with-start {
		 - struct date start;
		 - char name\[Len];
		 - in height;
		 - int weight;
		 - char gender;
		 - int idnum;
		 - short age;
		}

Array of structs
int main() {
	struct person persons\[100];
	
	persons\[1] = getstruct("Liz");
	persons[2] = getstruct("Jim");
	persons[2].idnum = 23456;
}

Referencing Array of structs
 - if (((persons\[4]).pno\[2]).areacode == 919)

structs as input parameters
 - void printname(struct person p)



