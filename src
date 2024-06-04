package calculator;
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;


public class Calculator implements ActionListener{
	JFrame frame;
	JTextField textfield;
	JButton[] numberbuttons = new JButton[10];
	JButton[] functionButtons = new JButton[10];
	JButton addButton,subButton,mulButton,divButton,equButton,decButton,delButton,clrButton,negButton,modButton;
	JPanel panel;
	
	
	Font myFont = new Font("Times new Roman",Font.BOLD,25);
	
	double num1=0,num2=0,result=0;
	char operator;
	
	Calculator(){
		
		frame = new JFrame("Calculator");
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.setSize(420, 550);
		frame.setLayout(null);
		
		textfield = new JTextField();
		textfield.setBounds(50,25,300,50);
        textfield.setFont(myFont);
        textfield.setEditable(false);
        
       
		
		addButton = new JButton("+");
		subButton = new JButton("-");
		mulButton = new JButton("*");
		divButton = new JButton("/");
		decButton = new JButton(".");
		equButton = new JButton("=");
		clrButton = new JButton("AC");
		delButton = new JButton("DE");
		negButton = new JButton("(-)");
		modButton = new JButton("%");
		
		
		functionButtons[0] = addButton;
		functionButtons[1] = subButton;
		functionButtons[2] = mulButton;
		functionButtons[3] = divButton;
		functionButtons[4] = decButton;
		functionButtons[5] = equButton;
		functionButtons[6] = clrButton;
		functionButtons[7] = delButton;
		functionButtons[8] = negButton;
		functionButtons[9] = modButton;
		
		
		
		for(int i=0; i<10; i++) {
			functionButtons[i].addActionListener(this);
			functionButtons[i].setFont(myFont);
			functionButtons[i].setFocusable(false);
		}
		for(int i=0; i<10; i++) {
			numberbuttons[i] = new JButton(String.valueOf(i));
			numberbuttons[i].addActionListener(this);
			numberbuttons[i].setFont(myFont);
			numberbuttons[i].setFocusable(false);
		}
		
			negButton.setBounds(50,430,75,50);
			delButton.setBounds(125, 430, 75, 50);
			clrButton.setBounds(200, 430, 75, 50);
			modButton.setBounds(275, 430, 75, 50);
			

			
			panel = new JPanel();
			panel.setBounds(50, 100,300,300);
			panel.setLayout(new GridLayout(4,4,-1,-1));
			panel.setBackground(Color.white);
			
			panel.add(numberbuttons[1]);
			panel.add(numberbuttons[2]);
			panel.add(numberbuttons[3]);
			panel.add(addButton);
			panel.add(numberbuttons[4]);
			panel.add(numberbuttons[5]);
			panel.add(numberbuttons[6]);
			panel.add(subButton);
			panel.add(numberbuttons[7]);
			panel.add(numberbuttons[8]);
			panel.add(numberbuttons[9]);
			panel.add(mulButton);
			panel.add(decButton);
			panel.add(numberbuttons[0]);
			panel.add(equButton);
			panel.add(divButton);
			
		frame.add(negButton);
		frame.setVisible(true);
		frame.add(delButton);
		frame.add(clrButton);
		frame.add(modButton);
		frame.add(panel);
		frame.add(textfield);
	}

	public static void main(String[] args) {
		
	           Calculator calc = new Calculator();
	}

	public void actionPerformed(ActionEvent e) {
		for(int i=0;i<10;i++) {
			if(e.getSource() == numberbuttons[i]) {
				textfield.setText(textfield.getText().concat(String.valueOf(i)));
			}
		}
		if(e.getSource() == decButton) {
			textfield.setText(textfield.getText().concat("."));
		}
		if(e.getSource() == addButton) {
			num1 = Double.parseDouble(textfield.getText());
			operator = '+';
			textfield.setText("");		
		}
		if(e.getSource() == subButton) {
			num1 = Double.parseDouble(textfield.getText());
			operator = '-';
			textfield.setText("");		
		}
		if(e.getSource() == mulButton) {
			num1 = Double.parseDouble(textfield.getText());
			operator = '*';
			textfield.setText("");		
		}
		if(e.getSource() == divButton) {
			num1 = Double.parseDouble(textfield.getText());
			operator = '/';
			textfield.setText("");	
		}
		if(e.getSource() == modButton) {
			num1 = Double.parseDouble(textfield.getText());
			operator = '%';
			textfield.setText("");
		}
		if(e.getSource() == equButton) {
			num2 = Double.parseDouble(textfield.getText());
			
			switch(operator) {
			case '+' :
				result = num1+num2;
				break;
			case '-' :
				result = num1-num2;
				break;
			case '*' :
				result = num1*num2;
				break;
			case '/' : 
				result = num1/num2;
				break;
			case '%' :
				result = num1%num2;
				break;
			}
			
			textfield.setText(String.valueOf(result));
			num1=result;
		}
		if(e.getSource() == clrButton) {
			textfield.setText("");
		}
		if(e.getSource() == delButton) {
			String string = textfield.getText();
			textfield.setText("");
			for (int i = 0;i<string.length()-1;i++) {
				textfield.setText(textfield.getText()+string.charAt(i));
			}
		}
		if(e.getSource() == negButton) {
			double temp = Double.parseDouble(textfield.getText());
			temp*=-1;
			textfield.setText(String.valueOf(temp));
		}	
	}
}
