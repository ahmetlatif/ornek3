package ornek3;

 
import java.io.BufferedReader;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.IOException;
import java.io.StreamTokenizer;
public class ornek3 {
 
    	public static void main(String[] args) throws InterruptedException,FileNotFoundException, IOException 
	{ 
		FileReader reader = new FileReader("MAKU.txt"); 
		BufferedReader bufferread = new BufferedReader(reader); 
		StreamTokenizer token = new StreamTokenizer(bufferread);  
		token.commentChar('a'); 
		int t; 
		while ((t = token.nextToken()) != StreamTokenizer.TT_EOF) 
		{ 
			switch (t) 
			{ 
			case StreamTokenizer.TT_NUMBER: 
				System.out.println("Sayı : " + token.nval); 
				break; 
			case StreamTokenizer.TT_WORD: 
				System.out.println("Metin : " + token.sval); 
				break; 

			} 
		} 
	} 
} 
