# Lab5






import java.util.Collections;
import java.util.LinkedList;
import java.util.List;
import java.util.Queue;
import java.util.Scanner;
import java.util.concurrent.ThreadLocalRandom;

public class songPlaylist {

	public static void main(String[] args) {
		
		
		String songTitle;
		int streamsAverageCount;
		String artistName;
		double artistAverage;
		
		
		streamsAverageCount = ThreadLocalRandom.current().nextInt(); 
		artistAverage = ThreadLocalRandom.current().nextDouble(); 
		
		Scanner input = new Scanner(System.in);
	      System.out.println("Enter an artist's name:");
	      
	      artistName = input.next();
		
	     Queue<String> songLine = new LinkedList<String>();
	      
	      songLine.add(artistName);  
	      
	      Scanner input2 = new Scanner(System.in);
	      System.out.println("Enter a song title name:");

	      songTitle = input2.next();
	      
	      Queue<String> artistLine = new LinkedList<String>();
	      
	      artistLine.add(songTitle);
	      
	      Collections.shuffle((List<?>) songLine);
	      System.out.println("Artist Queue: " + songLine);
	      System.out.println(songTitle +" Average count streams are: "+ streamsAverageCount );
	      
	      System.out.println("");
	      
	      Collections.shuffle((List<?>) artistLine);
	      System.out.println("Song Queue: " + artistLine);
	      System.out.println(artistName +" Artist's popularity average: "+ artistAverage);
	      
	     
	}

}
