import java.util.HashMap;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        HashMap<Character, Integer> hmap = new HashMap<Character, Integer>();
        Scanner kb = new Scanner(System.in);
        char[] arr1 = kb.nextLine().toCharArray();
        char[] arr2 = kb.nextLine().toCharArray();
        hmap.put('*', 0);

        for (int i = 0; i < arr2.length; i++){
            if (hmap.get(arr2[i]) == null){
                    hmap.put(arr2[i], 1);
            }else{
                hmap.put(arr2[i], hmap.get(arr2[i]) + 1);
            }
        }

        for (int i = 0; i < arr1.length; i++){
            if (hmap.get(arr1[i]) == null || hmap.get(arr1[i]) == 0){
                hmap.put('*', hmap.get('*') - 1);
            }else{
                hmap.put(arr1[i], hmap.get(arr1[i]) - 1);
            }
        }

        boolean anagram = true;

        for (Integer v : hmap.values()){
            if (v != 0){
                anagram = false;
            }
        }

        if (anagram){
            System.out.println('A');
        }else{
            System.out.println('N');
        }
    }
}
