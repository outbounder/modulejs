# Description #
commonjs/module like implementation for module based development within web/html applications
# Usage #
## export myMath module in /libs/myMath.js ##
    exports.mySum = function() {
      var sum = 0;
	  for(var i = 0; i<arguments.length; i++)
		sum += arguments[i];
      return sum;
    }
### using myMath ###
    var myMathModule = require("libs/myMath.js");
    myMathModule.mySum(10,20,30)
## export module class in /classes/myClass.js ##
    exports = function() {
    };
### using exported module class ###
    var myClass = require("classes/myClass.js");
    var myInstance = new myClass();
## using nested modules ##
    exports = function() {
      var myMath = require("/libs/myMath.js");
	  ....
    }
