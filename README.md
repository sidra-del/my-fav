import java.util.regex.*;
import java.util.*;

public class KeywordFinder {
    public static void main(String[] args) {
        String code = "int a = 5; if(a > 2) { System.out.println(a); } else { a = 10; }";
        String keywordPattern = "\\b(int|if|else|for|while)\\b";

        Pattern pattern = Pattern.compile(keywordPattern);
        Matcher matcher = pattern.matcher(code);

        System.out.println("Keywords found:");
        while (matcher.find()) {
            System.out.println(matcher.group());
        }
    }
}
