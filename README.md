https://spectreattack.com/spectre.pdf
论文里的代码例子，
原代码使用Dev-C++编译时会报错[Error] initializing argument 1 of 'long long unsigned int __rdtscp(unsigned int*)' [-fpermissive]，
发现void readMemoryByte()函数里，time1=__rdtscp(&junk)、time2=__rdtscp(&junk)中junk是int类型，
改正：把junk改为 unsigned int类型。 

机密是The Magic Words are Squeamish Ossifrage. 作者还玩了个RSA算法的梗。
