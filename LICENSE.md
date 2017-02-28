    function ListQ(a, b, N) {
      var temp;
      var arrayA = [];
      var arrayB = [];
      var array = [];
      var i,j;
      if(a>b) {
        temp = a;
        a = b;
        b = temp;
      }
      for(i=1;i<N;i++) {
        arrayA.push(i*a);
        arrayB.push(i*b);
      }
      for(i=0,j=0;i+j<N;) {
        if(arrayA[i] < arrayB[j]) {
          temp = arrayA[i];
          i++;
        } 
        else if(arrayA[i] == arrayB[j]) {
          temp = arrayA[i];
          i++;
          j++;
        }
        else {
          temp = arrayB[j];
          j++;
        }
        array.push(temp);
      }
      return array
    }
    
This are test data,you can change a, b, N for other test.

      var N = 8;
      var a = 3;
      var b = 5;
      var array = [];
      array = ListQ(a, b, N).join(',');
      console.log(array);
