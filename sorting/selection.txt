package sorting;

public class SelectionSort {

	public static void sSort(int[] arr) {
		int n = arr.length;
		for (int i = 0; i < n - 1; i++) {

			int minI = i;
			for (int j = i + 1; j < n; j++) {
				if (arr[j] < arr[minI]) {
					minI = j;
				}
			}
			int temp = arr[minI];
			arr[minI] = arr[i];
			arr[i] = temp;

		}

	}

	public static void main(String[] args) {
		int[] array = { 6, 10, 8, 9, 3, 2 };
		System.out.println("Array before sorted");
		for (int num : array) {
			System.out.print(num + " ");
		}
		System.out.println("   ");
		System.out.println("Array after sorted");
		sSort(array);
		for (int num : array) {
			System.out.print(num + " ");
		}
	}

}
