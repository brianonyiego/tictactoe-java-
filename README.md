# tictactoe-java-
#a program for the tictactoe game using java's GUI
#eclipse ide

package tictactoe;
import java.awt.*;
import java.awt.event.*;
import java.util.Random;

import javax.swing.*;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPanel;

public class tictac extends JFrame implements ActionListener {
Random random= new Random();

JPanel panel= new JPanel();
JPanel button_p= new JPanel();
JLabel text= new JLabel();
JButton [] button= new JButton[9];
boolean player_turn;
	
	tictac(){
	this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		this.setSize(800,800);
		this.getContentPane().setBackground(new Color(255,255,255));
		this.setLayout(new BorderLayout());
		this.setLocationRelativeTo(null);
		this.setVisible(true);
	
		
		text.setBackground(new Color(0,0,0));
		text.setForeground(new Color(25,255,0));
		text.setFont(new Font("ink free", Font.BOLD,75));
		text.setHorizontalTextPosition(JLabel.CENTER);
		text.setText("tic tactoe");
		text.setOpaque(true);
		
		
		
		
		panel.add(text);
		this.add(panel);
		this.add(panel,BorderLayout.NORTH);
		
		button_p.setLayout(new GridLayout(3,3));
		panel.setBounds(0,0,800,100);
		
		button_p.setLayout(new GridLayout(3,3));
		button_p.setBackground(new Color(0, 255, 0));
		 this.add(button_p);
		
		 for(int i = 0; i<9 ; i ++) {
			 button[i] = new JButton();
			 button_p.add(button[i]);
			 button[i].setFont(new Font("ink free", Font.BOLD,120));
			 button[i].setFocusable(false);
			 button[i].addActionListener(this);
			 
		 }
		firstturn();
	}
	@Override
	public void actionPerformed(ActionEvent e) {
		// TODO Auto-generated method stub
	for(int i =0; i<9;i++) {
	if(e.getSource() == button[i]) {
	if (player_turn) {
		if(button[i].getText()=="") {
			button[i].setForeground(new Color(255,0,0 ));
	        button[i].setText("O");
	        player_turn=false;
	        text.setText("o-turn");
		  check();
		
		}
	}
	else {
		button[i].setForeground(new Color(0,0,0 ));
        button[i].setText("O");
        player_turn=true;
        text.setText("O-turn");
		check();		
	}
		
		
	}
		}		
		
	}
	public void firstturn() {
		try {
			Thread.sleep(2000);
		} catch (InterruptedException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		
		if(random.nextInt(2)== 0) {
			player_turn=true;
			text.setText("x- turn");
		}
		else {
			player_turn=false;
			text.setText("o- turn");
		}
		
		
	}
	public void check() {
		if ( (button[0].getText()== "X") &&  
				(button[1].getText()== "X")
				&&
				(button[1].getText()== "X")) {
			
			xwins(0,1,2);
			
			
		}
		if ( (button[1].getText()== "X") &&  
				(button[4].getText()== "X")
				&&
				(button[7].getText()== "X")) {
			
			xwins(1,4,7);	
		}
		if ( (button[3].getText()== "X") &&  
				(button[4].getText()== "X")
				&&
				(button[5].getText()== "X")) {
			
			xwins(3,4,5);	
		}
		if ( (button[0].getText()== "X") &&  
				(button[4].getText()== "X")
				&&
				(button[8].getText()== "X")) {
			
			xwins(0,4,8);	
		}
		if ( (button[2].getText()== "X") &&  
				(button[4].getText()== "X")
				&&
				(button[6].getText()== "X")) {
			
			xwins(2,4,6);	
		}
		if ( (button[0].getText()== "X") &&  
				(button[1].getText()== "X")
				&&
				(button[1].getText()== "X")) {
			
			xwins(0,1,2);
			
			
		}
		if ( (button[1].getText()== "X") &&  
				(button[4].getText()== "X")
				&&
				(button[7].getText()== "X")) {
			
			xwins(1,4,7);	
		}
		if ( (button[3].getText()== "X") &&  
				(button[4].getText()== "X")
				&&
				(button[5].getText()== "X")) {
			
			xwins(3,4,5);	
		}
		if ( (button[0].getText()== "X") &&  
				(button[4].getText()== "X")
				&&
				(button[8].getText()== "X")) {
			
			xwins(0,4,8);	
		}
		if ( (button[2].getText()== "X") &&  
				(button[4].getText()== "X")
				&&
				(button[6].getText()== "X")) {
			
			xwins(2,4,6);	
			
			
		}
		if ( (button[0].getText()== "O") &&  
				(button[1].getText()== "O")
				&&
				(button[1].getText()== "O")) {
			
			owins(0,1,2);
			
			
		}
		if ( (button[1].getText()== "O") &&  
				(button[4].getText()== "O")
				&&
				(button[7].getText()== "O")) {
			
			owins(1,4,7);	
		}
		if ( (button[3].getText()== "O") &&  
				(button[4].getText()== "O")
				&&
				(button[5].getText()== "O")) {
			
			owins(3,4,5);	
		}
		if ( (button[0].getText()== "O") &&  
				(button[4].getText()== "O")
				&&
				(button[8].getText()== "O")) {
			
			owins(0,4,8);	
		}
		if ( (button[2].getText()== "O") &&  
				(button[4].getText()== "O")
				&&
				(button[6].getText()== "O")) {
			
			owins(2,4,6);	
			
			
		}
		if ( (button[0].getText()== "O") &&  
				(button[1].getText()== "O")
				&&
				(button[1].getText()== "O")) {
			
			owins(0,1,2);
			
			
		}
		if ( (button[1].getText()== "O") &&  
				(button[4].getText()== "O")
				&&
				(button[7].getText()== "O")) {
			
			owins(1,4,7);	
		}
		if ( (button[3].getText()== "O") &&  
				(button[4].getText()== "O")
				&&
				(button[5].getText()== "O")) {
			
			owins(3,4,5);	
		}
		if ( (button[0].getText()== "O") &&  
				(button[4].getText()== "O")
				&&
				(button[8].getText()== "O")) {
			
			owins(0,4,8);	
		}
		if ( (button[2].getText()== "O") &&  
				(button[4].getText()== "O")
				&&
				(button[6].getText()== "O")) {
			
			owins(2,4,6);	
		}
		
	}
	public void xwins(int a, int b , int  c) {
		button[a].setBackground(Color.green);
		button[b].setBackground(Color.green);
		button[c].setBackground(Color.green);
		
		for(int i =0 ; i<9;i++) {
			button[i].setEnabled(false);
		}
		text.setText("X-WINS");
		
	}
    public void owins(int a, int b , int  c) {
		button[a].setBackground(Color.green);
		button[b].setBackground(Color.green);
		button[c].setBackground(Color.green);
		
		for(int i =0 ; i<9;i++) {
			button[i].setEnabled(false);
		}
		text.setText("O-WINS");
		
	
	}

}



--------------------------------------------------------------------------------------------------------------------------------------------------------------------
#new java class in the same package , we deeclare the tictac class under the static void main method
package tictactoe;

public class main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
new tictac();
	}

}
