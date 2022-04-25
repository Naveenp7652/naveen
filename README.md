import java.io.*;
public class Example 
{
public static void main(String args[]) 
{
FileInputStream fis=null;
try
{

fis=new FileInputStream("/home/techvidvan/file.txt");
}
catch(FileNotFoundException fnfe)
{
System.out.println("the specified file is not"+"present at the given path");
}
int k;
try
{
while(  (k=fis.read())!= -1)
{
System.out.println((char)k);
}
fis.close();
}
catch(IOException ioe)
{
System.out.println("I/O error occured :"+ioe);
}
finally
{
System.out.println("happy");
}

}
}
