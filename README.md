# Question-1

  function sumOfDigitFactorial(number){

    for (var i = number - 1; i >= 1; i--) {
       number = parseInt(number * i);

    }

    let numberList = number.toString().split("");
    let z = 0;

    for (let j=0; j<numberList.length; j++){
      z = z + parseInt(numberList[j]);
    }

    return z;
  }

  console.log(sumOfDigitFactorial(100));
