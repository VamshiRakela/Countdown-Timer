# Countdown-Timer
This project displays the coundown using Java
import java.util.*;
import java.awt.*;
import java.awt.event.*;
class revclk implements ActionListener
{
	Frame f;
	Panel p;
	Label l1;
	Thread th1;
	String str,sr2;	
	//Calendar c1,c2;
	TextField txt1,txt2,txt3;
	Button b1;
	Font f1;
	revclk()
	{
		f=new Frame();
		p=new Panel();
		txt1=new TextField(20);
		txt2=new TextField(20);
		txt3=new TextField(20);
		l1=new Label("00:00:00");
		f1=new Font("Arial",Font.BOLD,34);
		l1.setFont(f1);
		p.add(l1);
		p.add(txt1);
		p.add(txt2);
		p.add(txt3);
		b1=new Button("Start");
		p.add(b1);
		f.add(p);
		f.setTitle("Clock");
		f.setSize(300,300);
		f.setVisible(true);
		
		b1.addActionListener(this);
	}
	public void actionPerformed(ActionEvent ae)
	{
		int hr1=Integer.parseInt(txt1.getText());//c1.set(Calendar.HOUR,txt1.getText());
		int min1=Integer.parseInt(txt2.getText());//c1.set(Calendar.MINUTE,txt2.getText());
		int sec1=Integer.parseInt(txt3.getText());//c1.set(Calendar.SECOND,txt3.getText());
		
		int hr2=0;
		int sec2=0;
		int min2=0;

		int hr3=0;
		int sec3=0;
		int min3=0;


		try
		{
			
			
			for(int i=0;i<=sec1;i++)
			{
				int sg=sec1-sec2;
				th1.sleep(300);
				String sd=hr1+":"+min1+":"+sg;
				l1.setText(sd);
				
				sec2++;
				
			}
		
			String sd=hr1+":"+min1+":"+00;
			l1.setText(sd);
			th1.sleep(300);
			sec2=0;
			sec1=59;
			min1--;
			 sd=hr1+":"+min1+":"+59;
			l1.setText(sd);

			
			while (true)
			{
				

				hr3=hr1-hr2;
				min3=min1-min2;
				sec3=sec1-sec2;

				sr2=hr3+":"+min3+":"+sec3;
				
				sec2++;
				l1.setText(sr2);
				if(sec2>59)
				{
					sec2=0;
					min2++;
				}
				if(min2>59)
				{
					hr2++;
					min2=0;
				}
				if(hr2>12)
				{
					hr2=0;
				}

				
				if(sec3<0)
				{
					min2--;
					sec1=61;
					
				} 
				if(min3<0)
				{
					hr1--;
					min1=60;
				}
				if(hr3<0)
				{
					hr1=11;
					min1=60;
					sec1=59;
				}

				
				
				th1.sleep(300);
			}

		}
		catch (Exception e)
		{
			System.out.println(e);
		}
	}


	public static void main(String[] args) 
	{
		new revclk();
	}
}

