int a = 6;
int* a_ptr = &a;
void * x = (void*) a_ptr;
int b = \*((int*) x)