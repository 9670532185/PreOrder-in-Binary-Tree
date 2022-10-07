# PreOrder-in-Binary-Tree

public class BinaryTreeNode<T> 
{
    T data;
    BinaryTreeNode<T> left;
    BinaryTreeNode<T> Right;
    BinaryTreeNode(T data)
    {
        this.data=data;
    }
    public static void PrintTree(BinaryTreeNode<Integer> root)
    {
        if(root==null)
        {
            return;
        }
        System.out.print(root.data +":");
        if(root.left !=null)
        {
            System.out.print("L :"+root.left.data+",");
        }
        if(root.Right!=null)
        {
            System.out.print("R :"+root.Right.data);
        }
        System.out.println();
        PrintTree(root.left);
        PrintTree(root.Right);
    }
    public static void Preorder(BinaryTreeNode<Integer> root)
    {
        if(root ==null)
        return;
        System.out.println(root.data);
        Preorder(root.left);
        Preorder(root.Right);
    }
    public static void main(String[] args)
    {
BinaryTreeNode<Integer> root=new BinaryTreeNode<Integer>(1);
BinaryTreeNode<Integer> rootleft=new BinaryTreeNode<Integer>(2);
BinaryTreeNode<Integer> rootRight=new BinaryTreeNode<Integer>(3);
BinaryTreeNode<Integer> TwoL=new BinaryTreeNode<Integer>(4);
BinaryTreeNode<Integer> TwoR=new BinaryTreeNode<Integer>(5);
root.left=rootleft;
root.Right=rootRight;
rootleft.left=TwoL;
rootRight.Right=TwoR;
//PrintTree(root);
//System.out.println(Preorder(root));
Preorder(root);

    }
    
}
