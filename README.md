#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <string.h>


int main()
{
   FILE *f;
   int MTO=0;//Tells if number is two or more digits. for bitshift
   char temp,line[200]; //temp= to hold charac line=to hold a one line
   int Cfx[20],x=0,Efx[20],Cgx[20],Egx[20],Chx[20],Ehx[20]; //Cfx=Constant of f(x) Efx=exponent of f(x) Cgx=Constant of g(x)
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
                                              for(MTO=0;fgetc(f)!='\n';MTO++)
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
                          printf("end of f function");                          
                          fgets(line,200,f);
                          for(x=0;fgetc(f)!='@';x++)
                          {
                                              fseek(f,-1,SEEK_CUR);       
                                              for(MTO=0;fgetc(f)!='x';MTO++)
                                              {      
                                                                        fseek(f,-1,SEEK_CUR);
                                                                        temp=fgetc(f);
                                                                        if(MTO!=0)    
                                                                            Cgx[x]=(Cgx[x]*10)+((int)temp-'0');                 
                                                                        else
                                                                            Cgx[x]=(int)temp-'0';                         
                                              }                           
                                                 printf(" %i",Cgx[x]);
                                              for(MTO=0;fgetc(f)!='\n';MTO++)
                                              {                                                                          
                                                               fseek(f,-1,SEEK_CUR);                              
                                                               temp=fgetc(f);                         
                                                               if(MTO!=0)    
                                                                            Egx[x]=(Egx[x]*10)+((int)temp-'0');                 
                                                               else
                                                                            Egx[x]=(int)temp-'0';
                                              }
                                                 printf(" %i",Egx[x]);
                                                  
                          }
                          printf("end of g function");                         
                          fgets(line,200,f);
                          for(x=0;fgetc(f)!='@';x++)
                          {
                                              fseek(f,-1,SEEK_CUR);       
                                              for(MTO=0;fgetc(f)!='x';MTO++)
                                              {      
                                                                        fseek(f,-1,SEEK_CUR);
                                                                        temp=fgetc(f);
                                                                        if(MTO!=0)    
                                                                            Chx[x]=(Chx[x]*10)+((int)temp-'0');                 
                                                                        else
                                                                            Chx[x]=(int)temp-'0';                         
                                              }                           
                                                 printf(" %i",Cgx[x]);
                                              for(MTO=0;fgetc(f)!='\n';MTO++)
                                              {                                                                          
                                                               fseek(f,-1,SEEK_CUR);                              
                                                               temp=fgetc(f);                         
                                                               if(MTO!=0)    
                                                                            Ehx[x]=(Ehx[x]*10)+((int)temp-'0');                 
                                                               else
                                                                            Ehx[x]=(int)temp-'0';
                                              }
                                                 printf(" %i",Egx[x]);
                           printf("end of h function");                       
                          }
   }while(false);
   getch();
}
                                              
                                              
                          
                          
                       
                       
                      
   
   
