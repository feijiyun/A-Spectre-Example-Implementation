https://spectreattack.com/spectre.pdf论文里的代码例子，
原代码使用Dev-C++编译时会报错[Error] initializing argument 1 of 'long long unsigned int __rdtscp(unsigned int*)' [-fpermissive]，
发现void readMemoryByte()函数里，time1=__rdtscp(&junk)、time2=__rdtscp(&junk)中junk是int类型，
改正：把junk改为 unsigned int类型。 
