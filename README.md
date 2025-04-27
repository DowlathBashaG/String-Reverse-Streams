# String-Reverse-Streams


✅ Reverse a String using pure Streams

		import java.util.List;
		import java.util.stream.Collectors;
		import java.util.stream.IntStream;

		public class ReverseStringUsingPureStreams {
			public static void main(String[] args) {
				String input = "HelloWorld";

				String reversed = IntStream.range(0, input.length())    // Create a stream of indexes
						.mapToObj(i -> input.charAt(input.length() - 1 - i)) // Map index to char in reverse order
						.map(String::valueOf)                           // Convert char to String
						.collect(Collectors.joining());                 // Join all characters

				System.out.println("Original: " + input);
				System.out.println("Reversed: " + reversed);
			}
		}
		
🛠️ How it works:

		Step	Explanation
		IntStream.range(0, input.length())	Stream of integers from 0 to length-1
  
		mapToObj(i -> input.charAt(length - 1 - i))	Fetch characters from end towards beginning
  
		map(String::valueOf)	Convert each character to String
  
		collect(Collectors.joining())	Join all characters together
		
⚡ Output:

		Original: HelloWorld
  
		Reversed: dlroWolleH

🎯 Key Points:

		Only used Streams operations (no external helper classes like StringBuilder).

		Full functional style.

		Clean and efficient.








