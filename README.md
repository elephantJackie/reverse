# reverse
给定一个 32 位有符号整数，将整数中的数字进行反转。假设我们的环境只能存储 32 位有符号整数，其数值范围是 [−231,  231 − 1]。根据这个假设，如果反转后的整数溢出，则返回 0。
var reverse = function(x) {
            var str = x.toString();
            var newStr = str.split("").reverse().join("");
            var afterNum = parseInt(newStr);
            var a = Math.pow(-2, 31);
            var b = Math.pow(2, 31) - 1;
            if (afterNum < a || afterNum > b) {
                return 0;
            } else {
                if(x < 0){
                    return afterNum * -1;
                }else{
                    return afterNum;
                }
            }
    };
