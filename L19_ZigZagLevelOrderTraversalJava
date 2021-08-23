class Solution {
    public List<List<Integer>> zigzagLevelOrder(TreeNode root) {
        Queue<TreeNode> queue = new LinkedList<TreeNode>();
        List<List<Integer>> wrapList = new LinkedList<List<Integer>>();
        
        if(root == null) return wrapList;
        
        queue.offer(root);
        boolean flag = true; 
        while(!queue.isEmpty()){
            int levelNum = queue.size();
            List<Integer> subList = new ArrayList<Integer>(levelNum);
            for(int i=0; i<levelNum; i++) {
                int index = i;
                if(queue.peek().left != null) queue.offer(queue.peek().left);
                if(queue.peek().right != null) queue.offer(queue.peek().right);
                if(flag == true) subList.add(queue.poll().val);
                else subList.add(0, queue.poll().val);
            }
            flag = !flag; 
            wrapList.add(subList);
        }
        return wrapList;
    }
}
