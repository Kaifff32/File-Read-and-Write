# File-Read-and-Write

package com.edubri;

import java.io.*;
import java.util.Scanner;

public class FileRW {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc=new Scanner(System.in);
		
		File f=new File("D:/Kaifff/k.txt");
		
		
		
		try {
			
			FileWriter fw=new FileWriter(f);
			BufferedWriter bw=new BufferedWriter(fw);
			System.out.println("Enter the First Line");
			bw.write(sc.nextLine()+"\n");
			System.out.println("Enter the Second Line");
			bw.write(sc.nextLine()+"\n");
			bw.flush();
			
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}

		 
		try {
			
			FileReader fr = new FileReader(f);
			BufferedReader bf=new BufferedReader(fr);
			String data=bf.readLine();
			System.out.println(data);
			while(data!=null)
			{
			data = bf.readLine();
			System.out.println(data);
			}
			
		} catch (FileNotFoundException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		
		
	}

}
