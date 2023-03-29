# Recursive-Binary-Search

    public static int binaryRec(int[] array, int target, int low, int high) {
        int mid = (low + high) / 2;
        if(low > high)
        {
            return -1;
        }
        if(array[mid] == target){
            return mid;
        }
        else if(array[mid]< target)
        {
            // mid +1 so that you dont get into infinite loop
            return binaryRec(array, target, mid+1, high);
        }
        else
        {
            return binaryRec(array, target, low, mid -1);
        }
    }
}
