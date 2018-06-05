#include<iostream.h>
#include<conio.h>
#include<stdio.h>
#include<dos.h>
#include<process.h>
#include<string.h>
#include<fstream.h>
char user[30];
int bn=-1,un=-1,temp=0;
ifstream fin("lib.dat",ios::binary);
ifstream fin2("log.dat",ios::binary);
class book
{
 int bno;
 char bname[30],author[20],cate[10],status[20],rate[5];
 void assign(int a)
 {
  if(a==1)
   strcpy(cate,"Education");
  else if(a==2)
   strcpy(cate,"Fiction");
  else if(a==3)
   strcpy(cate,"Comedy");
  else if(a==4)
   strcpy(cate,"Drama");
  else if(a==5)
   strcpy(cate,"Romantic");
  else
   strcpy(cate,"Unknown");
 }
 public:
 void get()
 {
  cout<<"\n\t\tEnter the book no.::";
  cin>>bno;
  cout<<"\n\t\tEnter the book name::";
  gets(bname);
  cout<<"\n\t\tEnter the author's name::";
  gets(author);
  cout<<"\n\t\tChoose the category:-\n\t\t1. Education  2. Fiction  3. Comedy  4. Drama  5. Romantic";
  cout<<"\n\t\tEnter the category::";
  int ch;
  cin>>ch;
  assign(ch);
  strcpy(status,"Available");
  cout<<"\n\t\tEnter the rating (in '*', min-*, max-*****)::";
  gets(rate);
  correctrate();
 }
 void put()
 {
  cout<<"\n\t\tBook no.     :: "<<bno;
  cout<<"\n\t\tBook name    :: "<<bname;
  cout<<"\n\t\tAuthor's name:: "<<author;
  cout<<"\n\t\tCategory     :: "<<cate;
  cout<<"\n\t\tStatus       :: "<<status;
  cout<<"\n\t\tRating       :: "<<rate;
 }
 int ret()
 {
  return bno;
 }
 void copynxt(int);
 void edit();
 int search(char[]);
 void copy(book);
 void setstatus(int);
 int checkstatus();
 void correctrate();
}b[10],a;
 void book::copynxt(int n)
 {
  bno=b[n].bno;
  strcpy(bname,b[n].bname);
  strcpy(author,b[n].author);
  strcpy(cate,b[n].cate);
  strcpy(rate,b[n].rate);
 }
 void book::edit()
 {
  cout<<"\n\t\t1. All\n\t\t2. Book no.\n\t\t3. Book name\n\t\t4. Author's name\n\t\t5. Category\n\t\t6. Status\n\t\t7. Rating";
  cout<<"\n\n\t\t\tEnter the section to be edited::";
  int c;
  cin>>c;
  switch(c)
  {
   case 1: cout<<"\n\t\tEnter the book no.::";
	   cin>>bno;
	   cout<<"\n\t\tEnter the book name::";
	   gets(bname);
	   cout<<"\n\t\tEnter the author's name::";
	   gets(author);
	   cout<<"\n\t\tChoose the category:-\n\t\t1. Education  2. Fiction  3. Comedy  4. Drama  5. Romantic";
	   cout<<"\n\t\tEnter the category::";
	   int ch;
	   cin>>ch;
	   assign(ch);
	   cout<<"\n\t\tChoose the status:-\n\t\t1. Available  2. Unavailable";
	   cout<<"\n\t\tEnter the category::";
	   cin>>ch;
	   setstatus(ch);
	   cout<<"\n\t\tEnter the rating (in '*', min-*, max-*****)::";
	   gets(rate);
	   break;
   case 2: cout<<"\n\t\tEnter the book no.::";
	   cin>>bno;
	   break;
   case 3: cout<<"\n\t\tEnter the book name::";
	   gets(bname);
	   break;
   case 4: cout<<"\n\t\tEnter the author's name::";
	   gets(author);
	   break;
   case 5: cout<<"\n\t\tChoose the category:-\n\t\t1. Education  2. Fiction  3. Comedy  4. Drama  5. Romantic";
	   cout<<"\n\t\tEnter the category::";
	   cin>>ch;
	   assign(ch);
	   break;
   case 6: cout<<"\n\t\tChoose the status:-\n\t\t1. Available  2. Unavailable";
	   cout<<"\n\t\tEnter the category::";
	   cin>>ch;
	   setstatus(ch);
	   break;
   case 7: cout<<"\n\t\tEnter the rating (in '*', min-*, max-*****)::";
	   gets(rate);
	   break;
   default:cout<<"\n\t\t\t!! INVALID CHOICE !!";
  }
 }
 int book::search(char s[])
 {
  for(int i=0;i<(bn+1);++i)
   if(strcmpi(b[i].bname,s)==0)
    return i;
  return -1;
 }
 void book::copy(book a)
 {
  bno=a.bno;
  strcpy(bname,a.bname);
  strcpy(author,a.author);
  strcpy(cate,a.cate);
  strcpy(rate,a.rate);
 }
 void book::setstatus(int a)
 {
  if(a==1)
   strcpy(status,"Available");
  else if(a==2)
   strcpy(status,"Unavailable");
  else if(a==3)
   strcpy(status,"Missing");
 }
 int book::checkstatus()
 {
  if(strcmp("Available",status)==0)
   return 1;
  return 0;
 }
 void book::correctrate()
 {
  for(int i=0;rate[i]!='\0';++i)
   if(rate[i]!='*')
    rate[i]='*';
 }
class usinfo
{
 int bkno;
 char addr[100],email[40];
 long ph;
 date d;
 public:
 long fee;
 char name[30];
 void get(int a)
 {
  strcpy(name,user);
  cout<<"\n\t\tEnter your phone no.:: ";
  cin>>ph;
  cout<<"\n\t\tEnter your e-mail ID:: ";
  cin>>email;
  cout<<"\n\t\tEnter your address(in single line using ',') ::\n\t\t";
  gets(addr);
  bkno=a;
  getdate(&d);
  fee=200.0;
 }
 void put()
 {
  cout<<"\n\t\tName          :: "<<name;
  cout<<"\n\t\tPhone no.     :: "<<ph;
  cout<<"\n\t\te-mail ID     :: "<<email;
  cout<<"\n\t\tAddress       :: "<<addr;
  cout<<"\n\t\tBook no.      :: "<<bkno;
  cout<<"\n\t\tDate of issued:: "<<(int)d.da_day<<":"<<(int)d.da_mon<<":"<<d.da_year;
  cout<<"\n\t\tFee           :: "<<calfee();
 }
 int ret()
 {
  return bkno;
 }
 void copynxt(int);
 long calfee();
}u[50];
 void usinfo::copynxt(int n)
 {
  ph=u[n].ph;
  strcpy(name,u[n].name);
  strcpy(email,u[n].email);
  strcpy(addr,u[n].addr);
  bkno=u[n].bkno;
  fee=u[n].fee;
 }
 long usinfo::calfee()
 {
  int a[3],b[3],c=0;
  date t;
  getdate(&t);
  a[0]=(int)t.da_day;a[1]=(int)t.da_mon;a[2]=t.da_year;
  b[0]=(int)d.da_day;b[1]=(int)d.da_mon;b[2]=d.da_year;
  c=a[2]-b[2];
  fee=fee+(c*500);
  c=a[1]-b[1];
  if( c<0 )
   c=c*(-1);
  fee=fee+(c*30);
  c=a[0]-a[0];
  if( c<0 )
   c=c*(-1);
  fee=fee+(c*2);
  return fee;
 }
void back1(char x)
{
  for(int i=0;i<78;++i)
   cout<<x;
  for(i=0;i<81;++i)
  {
   gotoxy(i,24);
   cout<<x;
  }
  gotoxy(1,2);
}
void clean()
{
  getch();
  clrscr();
  sound(1000);
  delay(50);
  nosound();
}
void msound()
{/*
 sound(100);delay(100);nosound();
 sound(600);delay(300);nosound();
 sound(800);delay(200);nosound();
 sound(400);delay(300);nosound();
 sound(800);delay(300);nosound();
 */
}
void welcome()
{
  gotoxy(24,10);
  cout<<"WELCOME TO PROGRAM";
  gotoxy(30,12);
  cout<<"*LIBSOFT*";
  gotoxy(31,13);
  cout<<"=======";
  gotoxy(35,15);
  msound();
  cout<<"Present By";
  gotoxy(38,16);
  cout<<"Jovial George";
}
void info1()
{
  gotoxy(50,22);
  cout<<"(Press Any Key To Continue)";
}
void info2()
{
  clean();
  back1('@');
  cout<<"\n\t\t\tRules\n\t\t\t=====\n\t1. You can only take one books at a time\n\t2. Submit the book as early as possible";
  cout<<"\n\t3. Please report if taken book is missing\n\t4. Fee will be automatically taken from your E-mail account";
}
int checkpw()
{
  char pw[20];
  for(int i=0;;++i)
  {
   pw[i]=getch();
   if(pw[i]==13)
   {
    pw[i]='\0';
    break;
   }
   gotoxy(46+i,12);
   cout<<"*";
  }
  int k;
  k=strcmp(pw,"god");
  if(k==0)
   return 1;
  return 0;
}
void addb()
{
 cout<<"\n\t\t\tEnter the no. of books to be added::";
 int n;
 cin>>n;
 info1();
 for(int i=0;i<n;++i)
 {
  clean();
  back1('+');
  b[++bn].get();
 }
 info1();
}
void viewb()
{
 if(bn==-1)
 {
  gotoxy(20,12);
  cout<<"!! SORRY, NO RECORDS TO DISPLAY !!";
 }
 for(int i=0;i<(bn+1);++i)
 {
  if(i%3==0&&i!=0)
  {
   clean();
   back1('+');
  }
  b[i].put();
  cout<<endl;
 }
 info1();
}
void delb()
{
 clean();
 back1('+');
 cout<<"\n\n\t\tEnter the book no. of book to be deleted::";
 int d,f=0;
 cin>>d;
 for(int i=0;i<(bn+1);++i)
 {
  if(d==b[i].ret())
  {
   for(int j=i;j!=bn;++j)
    b[j].copynxt(j+1);
   f=1;
   --bn;
   cout<<"\n\n\t\t\t"<<d<<" is deleted";
  }
 }
 if(f==0)
  cout<<"\n\n\t\t\t!! SORRY THIS BOOK NO. DOES NOT EXIST !!";
 info1();
}
void editb()
{
 clean();
 back1('+');
 cout<<"\n\t\t\tEnter the book no. to be edited::";
 int e,f=0;
 cin>>e;
 for(int i=0;i<(bn+1);++i)
  if(e==b[i].ret())
  {
   b[i].edit();
   f=1;
  }
 if(f==0)
  cout<<"\n\t\t\t!! SORRY, THIS BOOK NO. DOES NOT EXIST !!";
 info1();
}
void searchb()
{
 clean();
 back1('+');
 cout<<"\n\t\tEnter the name of the book to be searched::";
 char s[30];
 gets(s);
 int k=b[0].search(s);
 if(k==-1)
  cout<<"\n\n\t\t\t!! SORRY THIS BOOK DOES NOT EXIST !!";
 else
 {
  cout<<"\n\n\t\t\t!! FOUND !!";
  cout<<"\n\n\t\tThis book's info are:-\n";
  b[k].put();
 }
 info1();
}
void takeb()
{
 clean();
 back1('+');
 int f=0,k;
 cout<<"\n\t\tEnter the book no. of the book to be taken:: ";
 cin>>k;
 for(int i=0;i<(bn+1);++i)
 {
  if(k==b[i].ret())
  {
   for(int j;j<(un+1);++j)
    if(strcmpi(u[i].name,user)==0)
    {
     cout<<"\n\n\t\t!! SORRY, YOU CAN NOT TAKE ANY MORE BOOKS !!";
     info1();
     getch();
     return;
    }
   if(b[i].checkstatus()!=1)
   {
    cout<<"\n\n\t\t!! SORRY, THIS BOOK IS NOT AVAILABLE !!";
    break;
   }
   cout<<"\n\n\t\t\tPlease verify your details "<<user<<" :-";
   u[++un].get(k);
   b[i].setstatus(2);
   f=1;
  }
 }
 if(f==0)
  cout<<"\n\t\t!! SORRY, THIS BOOK DOES NOT EXIST !!";
 info1();
}
void subb(int c)
{
 clean();
 back1('+');
 int f=0;
 for(int i=0;i<(un+1);++i)
  if(strcmpi(user,u[i].name)==0)
  {
   if(c==2)
    u[i].fee+=2000;
   u[i].put();
   cout<<"\n\n\t\t!! FEES HAS BEEN WITHDRAWN FROM YOUR E-mail ACCOUNT !!";
   for(int j=0;j<(bn+1);++j)
    if(b[j].ret()==u[i].ret())
    {
     if(c==1)
      b[j].setstatus(1);
     else
      b[j].setstatus(3);
    }
   for(j=i;j!=un;++j)
    u[j].copynxt(j+1);
   --un;
   f=1;
  }
 if(f==0)
 {
  cout<<"\n\t\t!! SORRY, LibSoft IS GOING RESTART !!";
  cout<<"\n\t\t\tBECAUSE "<<user<<" HAVEN'T TAKEN ANY BOOK.";
  cout<<"\n\t\t\tRETYPE YOUR USER NAME AGAIN AND TRY AGAIN";
 }
 info1();
}
void viewu()
{
 if(un==-1)
 {
  gotoxy(20,12);
  cout<<"!! SORRY, NO RECORDS TO DISPLAY !!";
 }
 for(int i=0;i<(un+1);++i)
 {
  if(i%3==0&&i!=0)
  {
   clean();
   back1('+');
  }
  u[i].put();
  cout<<endl;
 }
 info1();
}
void quit()
{
 char r[5];
 char pr[30];
 clean();
 back1('$');
 gotoxy(30,8);
 cout<<"Thank you for using LibSoft\n";
 cout<<"\nPlease suggest this program for your friends , library office ,etc\n";
 cout<<"\nIf you have any problem with LibSoft please report it here(Enter N for nothing)::\n";
 gets(pr);
 if(pr[0]=='N')
  cout<<"OK\n";
 else
  cout<<"Your problem will be solved early as possible\n";
 cout<<"Please give your rating for this program(Enter as '*',maximum 5 stars)::\n\t\t\t";
 gets(r);
 if(r[0]=='*'&&r[1]=='*'&&r[2]=='*'&&r[3]=='*'&&r[4]=='*')
  cout<<"\n\t\t\t\t\1\1\1 AWESOME \1\1\1\n";
 else if(r[0]=='*'&&r[1]=='*'&&r[2]=='*'&&r[3]=='*')
  cout<<"\n\t\t\t\t\1\1 VERY GOOD \1\1\n";
 else if(r[0]=='*'&&r[1]=='*'&&r[2]=='*')
  cout<<"\n\t\t\t\t\1 GOOD \1\n";
 else if(r[0]=='*'&&r[1]=='*')
  cout<<"\n\t\t\t\t\1 NOT BAD \7\n";
 else if(r[0]=='*')
  cout<<"\n\t\t\t\t\7 BAD \7\n";
 else
  cout<<"\n?? Nothing ??\n";
 cout<<"\n\t\tThank you again\n";
 cout<<"\t\t\tCatch you later";
 info1();
 fin.close();
 ofstream fout("lib.dat",ios::binary);
 ofstream fout2("log.dat",ios::binary);
 for(int i=0;i<(bn+1);++i)
  fout.write((char*)&b[i],sizeof(b[i]));
 for(i=0;i<(un+1);++i)
  fout2.write((char*)&u[i],sizeof(u[i]));
 fout.close();
 fout2.close();
 getch();
 exit(0);
}
void adminp()
{
 ADMIN:
 clean();
 back1('#');
 gotoxy(35,2);
 cout<<"MENU (Administer mode)";
 gotoxy(34,3);
 cout<<"======";
 cout<<"\n\t\t1. Add a book";
 cout<<"\n\t\t2. Edit a book";
 cout<<"\n\t\t3. Delete a book";
 cout<<"\n\t\t4. View the lib-table";
 cout<<"\n\t\t5. View the user-log";
 cout<<"\n\t\t6. Search a book";
 cout<<"\n\t\t7. To go back";
 cout<<"\n\t\t 0. Exit";
 cout<<"\n\n\t\t\tEnter your choice::";
 int ch;
 cin>>ch;
 info1();
 switch(ch)
 {
  case 1: clean();
	  back1('#');
	  addb();
	  break;
  case 2: editb();
	  break;
  case 3: delb();
	  break;
  case 4: clean();
	  back1('+');
	  viewb();
	  break;
  case 5: clean();
	  back1('+');
	  viewu();
	  break;
  case 6: searchb();
	  break;
  case 7: return;
  case 0: quit();
	  break;
  default:cout<<"\n\t\t\t!! INVALID CHOICE !!";
 }
 goto ADMIN;
}
void guest()
{
 info2();
 GUEST:
 clean();
 back1('#');
 gotoxy(35,2);
 cout<<"MENU (Guest mode)";
 gotoxy(34,3);
 cout<<"======";
 cout<<"\n\t\t1. Take a book";
 cout<<"\n\t\t2. Submit book";
 cout<<"\n\t\t3. View books";
 cout<<"\n\t\t4. Search a book";
 cout<<"\n\t\t5. Report book is missing";
 cout<<"\n\t\t6. To go back";
 cout<<"\n\t\t 0. Exit";
 int ch;
 cout<<"\n\n\t\t\tEnter your choice::";
 cin>>ch;
 switch(ch)
 {
  case 1: takeb();
	  break;
  case 2: subb(1);
	  return;
  case 3: clean();
	  back1('+');
	  viewb();
	  break;
  case 4: searchb();
	  break;
  case 5: subb(2);
	  return;
  case 6: return;
  case 0: quit();
	  break;
  default:cout<<"\n\t\t\t!! INVALID CHOICE !!";
 }
 goto GUEST;
}
void main()
{
 clrscr();
 back1('#');
 welcome();
 if(!fin&&!fin2)
 {
  cout<<"\n\t\t!! SORRY FILES IS NOT ATTACHED !!";
  quit();
 }
 info1();
 int i=0;
 while(fin.read((char*)&b[i],sizeof(b[i])))
 {
  ++bn;
  ++i;
 }
 i=0;
 while(fin2.read((char*)&u[i],sizeof(u[i])))
 {
  ++un;
  ++i;
 }
 while(1)
 {
 clean();
 back1('*');
 int ch;
 cout<<"\t\t\t\tLOGIN AS\n";
 cout<<"\t\t\t\t========\n\n";
 cout<<"\n\t\t1. Administer\n";
 cout<<"\n\t\t2. Guest\n";
 cout<<"\n\nNote:( Guest mode can not make changes in any of the datas in this program.";
 cout<<"\n      Enter 1 if you want administer mode or 2 if guest mode.";
 cout<<"\n      Enter 0 to exit from libsoft.)\n";
 cout<<"\n\n\t\tEnter the mode of user::";
 cin>>ch;
 if(ch==1)
 {
  int c=4;
  cout<<"\n\t\t\tAdiminister mode is accepted\n";
  info1();
  pass:
  clean();
  back1('@');
  gotoxy(23,3);
  cout<<"Welcome To Administer Mode";
  gotoxy(23,4);
  cout<<"==========================";
  gotoxy(25,10);
  cout<<"Enter Your Name:: ";
  gets(user);
  gotoxy(25,12);
  cout<<"Enter The Password:: ";
  int k=checkpw();
  if(k==1)
  {
   cout<<"\n\n\t\t\tPassword Accepted";
   info1();
   adminp();
  }
  else
  {
   cout<<"\n\n\t\t\tPassword Not Accepted";
   cout<<"\n\n\t\tYou have "<<c-1<<" more chance to try";
   --c;
   info1();
   if(c==0)
   {
    cout<<"\n\t\t\tYour chance is over, Try again later";
    quit();
   }
   goto pass;
  }

 }
 else if(ch==2)
 {
  cout<<"\n\t\t\tGuest mode is accepted\n";
  info1();
  clean();
  back1('@');
  gotoxy(25,10);
  cout<<"Enter Your Name:: ";
  gets(user);
  cout<<"\n\t\t\tWelcome "<<user;
  info1();
  guest();
 }
 else if(ch==0)
 {
  info1();
  quit();
 }
 else
 {
  cout<<"\n\t\t\t!! INVALID CHOICE !!\n";
  info1();
 }
}
}