# Rectangle
## A problem in java
Write a Java program that prompts a user to enter the length and width of a rectangle and then proceeds to render a rectangle of the dimensions entered on the computer screen.
## Solution
### Java code
//rectangle.java
import javax.swing.*;
import java.util.Scanner;
import java.awt.*;
public class Assignment1a extends JPanel {
    @Override
public void paint(Graphics g){
    Scanner s=new Scanner(System.in);
  System.out.println("Enter the length of the rectangle you wish to draw in pixels:");
double len=s.nextDouble();
System.out.println("Enter the width of the rectangle you wish to draw in pixels:");
double wid=s.nextDouble();
g.drawRect(100, 100,(int)len,(int)wid); //starting from position (100,100) on screen coordinates
System.out.println("Now go to the frame to get a rectangle of your dimensions");

}
    public static void main(String[] args) {
        JFrame f=new JFrame("Please don't minimize this window,click the cursor out of this window to enter length and width!");
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        f.getContentPane().add(new Assignment1a());
        f.setSize(700,600);
        f.setLocation(100,50);
        f.setVisible(true);
    }
    
}

## Compiled code
###### Includes the above code + the compiled class
[compiled.zip](https://github.com/SimonDouglas-bit/Rectangle/files/9615851/compiled.zip)
