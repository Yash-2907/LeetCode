class Solution {
    public boolean areSentencesSimilar(String sentence1, String sentence2) {
        String[] words1 = sentence1.split(" ");
        String[] words2 = sentence2.split(" ");

        int n1 = words1.length;
        int n2 = words2.length;

        // Check if the sentences have the same length
        if (n1 == n2) {
            // Compare words one by one
            for (int i = 0; i < n1; i++) {
                if (!words1[i].equals(words2[i])) {
                    return false;
                }
            }
            return true;
        }

        // Handle cases where lengths are different
        // Logic to check if one sentence can be derived from the other
        // For simplicity, you might want to just check the start and end words

        // Similarity condition (both sentences can be reduced)
        int i = 0, j = 0;

        // Compare from the start
        while (i < n1 && i < n2 && words1[i].equals(words2[i])) {
            i++;
        }

        // Compare from the end
        while (j < n1 - i && j < n2 - i && words1[n1 - 1 - j].equals(words2[n2 - 1 - j])) {
            j++;
        }

        // If we have crossed over the sentence bounds, then they are similar
        return i + j >= Math.min(n1, n2);
    }
}
