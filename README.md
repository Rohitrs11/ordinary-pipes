//# ordinary-pipes
ordinary pipes


#include<stdio.h>
#include<sys/types.h>
#include<sys/stst.h>
#include<fcntl.h>
#include<string.h>
#include<stdlib.h>
#include<unistd.h>
#include<sys/wait.h>
#define size 20

int main(int arg,char* ar[])
{
intf[2];
pid_t c_id;
char rBuffer[size];
pipe(file);
if(arg !=3)
{
printf("error : Need exactly two parameters.\n");
exit(1);
}
int fOpen=open(ar[1], 0);
int Targetfile =open(ar[2], O_RDWR\O_CREATE|O_APPEND,0666);
if(fopen== -1|| targetfile ==-1)
{
printf("file cannot be opened\n");
exit(1);
}
c_id=fork();
if(c_id==0)
{
close(f[1]);
while(read(f[0], rBuffer,size of (rBuffer)>0)
{
write(Targetfile,rBuffer,strlen(rBuffer) -1);
}
close(f[0]);
close(Targetfile);
}
else
{
close(f[0]);
while(read(fOpen),rBuffer,size of (rBuffer)>0);
{
write (f[1] ,rBuffer, size of (rBuffer));
memset(r,Buffer,0,size);
}
close(f[1]);
close(fOpen);
wait(NULL);
}

}
