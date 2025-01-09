# file-handling-utility-

import java.io.BufferedWriter;
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class FileHandlingExample {
    public static void main(String[] args) {
        
        File file = new File("example.txt");

        
        try (BufferedWriter writer = new BufferedWriter(new FileWriter(file))) {
            writer.write("Hello, this is a sample file handling program in Java.");
            writer.newLine(); 
            writer.write("This line is written to the file.");
        } catch (IOException e) {
            e.printStackTrace();
        }

        System.out.println("File written successfully.");
    }
}
