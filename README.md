#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <string.h>


int main()
{
   FILE *f;
   int MTO=0;//Tells if number is two or more digits. for bitshift
   char temp;
   int Cfx[20],x=0,Efx[20],Cgx[20],Egx[20]; //Cfx=Constant of f(x) Efx=exponent of f(x) Cgx=Constant of g(x)
   f=fopen("week2.txt","r");
   do
   {
                          for(x=0;fgetc(f)!='@';x++)
                          {
                                              fseek(f,-1,SEEK_CUR);       
                                              for(MTO=0;fgetc(f)!='x';MTO++)
                                              {      
                                                                        fseek(f,-1,SEEK_CUR);
                                                                        temp=fgetc(f);
                                                                        if(MTO!=0)    
                                                                            Cfx[x]=(Cfx[x]*10)+((int)temp-'0');                 
                                                                        else
                                                                            Cfx[x]=(int)temp-'0';                         
                                              }                           
                                                 printf(" %i",Cfx[x]);
                                              for(MTO=0;temp=fgetc(f)!='\n';MTO++)
                                              {                                                                          
                                                               fseek(f,-1,SEEK_CUR);                              
                                                               temp=fgetc(f);                         
                                                               if(MTO!=0)    
                                                                            Efx[x]=(Efx[x]*10)+((int)temp-'0');                 
                                                               else
                                                                            Efx[x]=(int)temp-'0';
                                              }
                                                 printf(" %i",Efx[x]);
                                                  
                          }
                          printf("end");
   }while(false);
   getch();
}
                                              
                                              
                          
                          
                       
                       
                      
   
   
