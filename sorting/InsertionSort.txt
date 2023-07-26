package sorting;

public class InsertionSort {
	public static void insertionSort(int[] arr) {
		int n = arr.length;
		for (int i = 0; i < n; i++) {
			int key = arr[i];
			int j = i - 1;

			while (j >= 0 && arr[j] > key) {
				arr[j + 1] = arr[j];
				j--;

			}
			arr[j + 1] = key;

		}
	}

	public static void main(String[] args) {
		int[] array = { 2, 1, 11, 9, 7, 404, 101, 81 };
		System.out.println("Array before sorting...");
		for (int num : array) {
			System.out.print(num + " ");
		}
		System.out.println(" ");
		System.out.println("Array after sorting...");
		insertionSort(array);
		for (int num : array) {
			System.out.print(num + " ");
		}
	}
}
