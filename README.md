PupilPath Plus
=================
A userscript which calculates and shows your total average.

Features
--------
* Average Calculator

Credits
------------
Average Calculation is done using [this](https://gist.github.com/cqfllp/1c2ccc83733fb1d4264a3785b14249d1) code, written by [cqfllp](https://github.com/cqfllp).
```javascript
  var links=document.querySelectorAll('tr[style="cursor: pointer"]');
  var text="";
  var num=0;
  var count=0;
  for(var i=0;i<links.length;i++){
    var str = links[i].innerText;
    text=str.split('MP1:  ')[1];
    text=parseFloat(text);
    text = text || 0;
    if (text==0){
    }else{
    num+=parseFloat(text);
    count++;
    }
  }
  var avg=num/count;
  alert("Total Average: "+Math.ceil(avg*100)/100);
```

Changelog
---------
* Version 1.3:
    - Added support for more Marking Periods.
* Version 1.2:
    - Added in jQuery.
* Version 1.0:
	- Created userscript.
