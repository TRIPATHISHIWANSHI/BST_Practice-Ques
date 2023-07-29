class BSTNode1{
	int data;
	BSTNode1 left;
	BSTNode1 right;
	public BSTNode1(Integer data) {
		this.data = data;
	}
}
public class StructrualCheck {

	BSTNode1 root1;
	BSTNode1 root2;
	void treeValues() {
		root1 = insert(root1,20);
		BSTNode1 t = insert(root1,10);
		t = insert(root1,30);
		t = insert(root1,7);
		t = insert(root1,15);
		print(root1);
		System.out.println();
		
		root2 = insert(root2,50);
		BSTNode1 t2 = insert(root2,40);
		t2 = insert(root2,60);
		t2 = insert(root2,30);
		t2 = insert(root2,45);
		print(root2);
		System.out.println();
		
		System.out.println((check(root1,root2))?"Identical":"Not Identical");
	}
	BSTNode1 insert(BSTNode1 curNode,int data){
		// check if root is not present
		if(curNode == null) {
			curNode = new BSTNode1(data);
			return curNode;
		}
		// root is present
		if(data<curNode.data) {
			curNode.left = insert(curNode.left,data);
		}
		else if(data>curNode.data) {
			curNode.right = insert(curNode.right,data);
		}
		return curNode;
	}
	void print(BSTNode1 curNode) { //Create a Print Function
		if(curNode!=null) {
			print(curNode.left);
			System.out.print(curNode.data+" ");
			print(curNode.right);
		}
	}
	
	boolean check(BSTNode1 curNode1, BSTNode1 curNode2) {
		if(curNode1==null && curNode2==null)return true;
		else if(curNode1!=null && curNode2!=null && 
				(curNode1.left==null && curNode2.left!=null) || 
				(curNode1.right==null && curNode2.right!=null)|| 
				
				(curNode1.left!=null && curNode2.left==null) || 
				(curNode1.right!=null && curNode2.right==null)) {
			return false;
		}
		return check(curNode1.left, curNode2.left)&& check(curNode1.right,curNode2.right);
	}
	
	public static void main(String[] args) {
		StructrualCheck obj = new StructrualCheck();
		obj.treeValues();
	}

}
