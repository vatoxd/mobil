int count_whites(const char string[]){ 
 	int result = 0; 
 	if (string == NULL){
 		return -1; 
 	} 
 	for (int i = 0; i < strlen(string); i++){ 
 		if (string[i] == ' '|| string[i] == '\t' || string[i] == '\n' ) { result = result +1; }
 		} 
 	return result; 
}

//3

int count_zeroes_2d(const int size, int array[][size]) {
    if (array == NULL) {
        return -1; 
    }

    int count = 0; 

    for (int i = 0; i < size; i++) {
        for (int j = 0; j < size; j++) {
            if (array[i][j] == 0) {
                count++; 
            }
        }
    }

    return count;
}


int longest_row(const int rows, const int cols, char array[rows][cols]) {
    if (array == NULL || rows < 1 || cols < 1) {
        return -1; 
    }

    int max_length = 0; 
    int max_index = 0; 

    for (int i = 0; i < rows; i++) {
        int current_length = 0; 

        for (int j = 0; j < cols && array[i][j] != '\0'; j++) {
            current_length++; 
        }

        if (current_length > max_length) {
            max_length = current_length; 
            max_index = i; 
        }
    }

    return max_index;
}

int is_vowel(const char c) {
  if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u' ||
      c == 'A' || c == 'E' || c == 'I' || c == 'O' || c == 'U') {
    return 1;
  }
  else {
    return 0;
  }
}


int is_in_array(const int num, const int size, const int array[]) {
  for (int i = 0; i < size; i++) {
    if (array[i] == num) {
      return 1;
    }
  }
  return 0;
}

char make_direction(const char karel) {
  if (karel == '>') {
    
    return 'E';
  }
  else if (karel == '^') {
    
    return 'N';
  }
  else if (karel == '<') {
    
    return 'W';
  }
  else if (karel == '_') {
   
    return 'S';
  }
  else {
    
    return '?';
  }
}

int is_prime(const int num) {
    if (num <= 1) return 0;
    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0) 
        	return 0;
    }
    return 1;
}
