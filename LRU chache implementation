import java.io.*;
import java.util.*;
class Node{
    int data;
    Node prev;
    Node next;
    Node(int data){
        this.data = data;
        prev = next = null;
    }

}
public class Main {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int t = sc.nextInt();
        while(t-->0){
            int n = sc.nextInt();
            int k = sc.nextInt();
            int[] arr = new int[n];
            for(int i=0;i<n;i++){
                arr[i] = sc.nextInt();
            }
            Node dummy = new Node(-1);
            Node tail = dummy;
            // dummy.next = tail;
            // tail.prev = dummy;
            Map<Integer,Node> map = new HashMap<>();
            for(int i=0;i<n;i++){
                int val = arr[i];
                if(map.containsKey(val)){
                    Node index = map.get(val);
                    if(index.prev!=null) {
                        index.prev.next = index.next;
                        
                    }
                    if(index.next!=null){
                        index.next.prev = index.prev;
                    }
                    else{
                        // index.prev.next = null;
                        tail = index.prev;
                    }
                    map.remove(val);
                }  
                    // tail.next = nn;
                    // nn.prev = tail;
                    // tail = tail.next;
                    // map.put(val,nn);
                else if(map.size()>=k){
                        Node temp = dummy.next;
                        // dummy.next = temp.next;
                        // temp.next.prev = dummy;
                        // dummy.next.next = dummy.next.next.next;
                        // dummy.next.prev = dummy;
                        if(temp!=null){
                            dummy.next = temp.next;
                            if(temp.next!=null){
                                temp.next.prev = dummy;
                            }else{
                                tail = dummy;
                            }
                            map.remove(temp.data);
                        }
                    }
                    Node nn = new Node(val);
                    if(dummy.next==null){
                        dummy.next = nn;
                        nn.prev = dummy;
                        // nn.prev = dummy;
                        tail = nn;
                    }else{
                        tail.next = nn;
                        nn.prev = tail;
                        tail = nn;
                    }
                    map.put(val,nn);
                }
            
            Node tep = dummy.next;
            while(tep!=null){
                System.out.print(tep.data+" ");
                tep = tep.next;
            }
            System.out.println();
        }
    }
}
