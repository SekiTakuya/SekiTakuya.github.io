---
layout: page
title: Regex
permalink: /regex/regex/
---
<script type="text/javascript">
<!--
function replaceRegEx(targetId, regExId, newValueId, resultId){
	var regEx = new RegExp($("#" + regExId).val(), "g");
	$("#" + resultId).val($("#" + targetId).val().replace(regEx, $("#" + newValueId).val()));
}
function getReplaceTxt(id, target, regEx, newValue){
	document.open();
	document.write(stringFormat("<input type=\"text\" id=\"target{0}\" value=\"{1}\" size=5 />", id, target));
	document.write(".replace(/");
	document.write(stringFormat("<input type=\"text\" id=\"regEx{0}\" value=\"{1}\" size=5 />", id, regEx));
	document.write("/g, \"");
	document.write(stringFormat("<input type=\"text\" id=\"newValue{0}\" value=\"{1}\" size=5 />", id, newValue));
	document.write("\")");
	document.write(stringFormat("<input type=\"button\" value=\"=\" onclick=\"replaceRegEx('target{0}','regEx{0}','newValue{0}','result{0}')\"/>", id));
	document.write(stringFormat("<input type=\"text\" id=\"result{0}\" value=\"\" size=10 />", id));
	document.close();
}
var stringFormat = function(fmt){
	for(var i = 0; i < arguments.length - 1; i++){
		fmt = fmt.replace(new RegExp("\{" + i + "\\}", "g"), arguments[i+1]);
	}
	return fmt;
}
//-->
</script>

## Matches Any Character

```
.
```

<script type="text/javascript">
<!--
getReplaceTxt("idAny","abcd",".","a");
//-->
</script>
<br/>

## Matches Number Character

```
\d
```

<script type="text/javascript">
<!--
getReplaceTxt("idNumber1","a1b2","\\d","Num");
//-->
</script>
<br/>
```
[0-9]
```

<script type="text/javascript">
<!--
getReplaceTxt("idNumber2","a1b2","[0-9]","Num");
//-->
</script>
<br/>

## Matches Alphabet Character

```
\D
```

<script type="text/javascript">
<!--
getReplaceTxt("idAlpha","a1b2","\\D","A");
//-->
</script>
<br/>
