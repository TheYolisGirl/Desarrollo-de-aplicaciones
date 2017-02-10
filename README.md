# Desarrollo-de-aplicaciones
// Figura 28.14: LineasRectangsElips.java
 // Dibuja líneas, rectángulos y elipses
0 import java.awt.*;
0 import java.awt.event.*;
0 import javax.swing.*;
public class LineasRectangsElips extends JFrame {
0 private String s = “Utilizando drawString!”;
0
 public LineasRectangsElips()
 {
 super( “Dibujando lineas, rectangulos y elipses” );

 setSize( 400, 165 );
 show();
 } // fin del constructor LineasRectangsElips

 public void paint( Graphics g )
 {
 g.setColor( Color.red );
 g.drawLine( 5, 30, 350, 30 );

 g.setColor( Color.blue );
 g.drawRect( 5, 40, 90, 55 );
 g.fillRect( 100, 40, 90, 55 );

 g.setColor( Color.cyan );
 g.fillRoundRect( 195, 40, 90, 55, 50, 50 );
 g.drawRoundRect( 290, 40, 90, 55, 20, 20 );

 g.setColor( Color.yellow );
 g.draw3DRect( 5, 100, 90, 55, true );
 g.fill3DRect( 100, 100, 90, 55, false );

 g.setColor( Color.magenta );
 g.drawOval( 195, 100, 90, 55 );
 g.fillOval( 290, 100, 90, 55 );
 } // fin del método paint

 public static void main( String args[] )
 {
 LineasRectangsElips app = new LineasRectangsElips();

 app.addWindowListener(
 new WindowAdapter() {
 public void windowClosing( WindowEvent e )
 {
 System.exit( 0 );
 } // fin del método windowClosing
 } // fin de la clase interna anónima
 ); // fin de addWindowListener
 } // fin de main
 } // fin de la clase LineasRectangsElips
