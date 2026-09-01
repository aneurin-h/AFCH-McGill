

MT: 2026-10-06 & 2026-11-19


\# incude algorithm

std::pair<int, int> getGreatestElement(int* arr){
			int maxVal;
			int maxIndex = 0;
		if(sizeof(arr)/sizeof(int) > 0) {
			maxVal = arr[0];
		} else {
			return {0, -1};
		}

		for(int i = 0; i < sizeof(arr)/sizeof(int); i++){
				if(arr[i] > maxVal){
					maxVal = arr[i];
					maxIndex = i;
				}
		}
		return {maxVal, maxIndex};
}