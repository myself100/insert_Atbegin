# insert_Atbegin

package elclipse;

public class NewNode {

	public static class ListNode{
		private int data;
		private ListNode next;

		public ListNode(int data) {
			this.data=data;
			this.next=null;
		}
	}

	public ListNode insertatbegin(ListNode head,int data) {
		ListNode newNode=new ListNode(data);
		if(head==null) {
			return newNode;
		}
		newNode.next=head;
		head=newNode;

		return head;
	}
	public static void display(ListNode head) {
		if(head==null) {
			return;
		}
		ListNode current= head;
		while(current!=null) {
			System.out.print(current.data + " --> ");              ////printing linkedlist
			current = current.next;
		}
		System.out.println(current);


	}
	public static void main(String[] args) {
		// TODO Auto-generated method stub

		ListNode head =new ListNode(1);
		ListNode second=new ListNode(2);
		ListNode third =new ListNode(3);
		ListNode fourth=new ListNode(4);

		head.next=second;
		second.next=third;
		third.next=fourth;

		NewNode newnod=new NewNode();
		ListNode newhead = newnod.insertatbegin(head,115);
		NewNode.display(newhead);                                   ////calling displaying function
	}

}
