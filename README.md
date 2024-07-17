# String-practice
有一个不定长度的String，其中前面是字母，后边是数字,例如："abcd123.456", 要求写一个方法得到其中的数字以String的形式返回,数字保留小数点后两位， 不四舍五入，截去多余小数,例如："abcd123.456"，得到"123.45" 如果数字没有小数点,要得到两位为0的小数，例如："abcd123"，得到"123.00".

1、String.valueOf(1.23)

2、 public String getString(String str){

 String getNumber;

 getNumber = str.replaceAll("[a-z|A-Z]", "");

 if(getNumber.indexOf(".") == -1){

  getNumber = getNumber+".00";

  }else {

  if(getNumber.indexOf(".")== getNumber.length()-1){

    getNumber= getNumber+"00";

   }else if (getNumber.indexOf(".")== getNumber.length()-2){

   getNumber = getNumber+"0";

   }else {

   getNumber = getNumber.substring(0, getNumber.indexOf(".")+3);

   }

  }

 return getNumber;

 } 
