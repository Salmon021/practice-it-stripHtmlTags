# practice-it-stripHtmlTags
Write a method called stripHtmlTags that accepts a Scanner representing an input file containing an HTML web page as its parameter, then reads that file and prints the file's text with all HTML tags removed. A tag is any text between the characters &lt; and > . 

public static void stripHtmlTags(Scanner input) {
    int start; int end;
    
    while (input.hasNextLine()) {
        String line = input.nextLine();        
        while (line.contains("<")) {
             start = line.indexOf("<");
             end = line.indexOf(">");             
            if (start != -1 && end != -1){
                String word = line.substring(start, end + 1);
                 line = line.replace(word, "");
            }
        }
        System.out.println(line);
    }
}
