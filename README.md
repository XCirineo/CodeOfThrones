#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <string.h>


int main()
{
   FILE *f;
   char *temp;
   int Cfx[20],x=0; //Cfx=Constant of f(x) 
   f=fopen("week2.txt","r");
   do
   {
                          for(x=0;fgetc(f)!='@';x++)
                          {
                                              fseek(f,-1,SEEK_CUR);       
                                              while(fgetc(f)!='x')
                                              {      
                                                                        fseek(f,-1,SEEK_CUR);
                                                                        *temp=fgetc(f);
                                                                        
                                                                        
                                              }
                                              Cfx[x]=(int)temp-'0';
                          }
   }while(false);
   printf("%i",Cfx[0]);
   getch();
}
                                              
                                              
                          
                          
                       
                       
                      
   
   
