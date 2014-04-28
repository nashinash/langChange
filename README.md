langChange
==========

langChange is simple pure javascript script for change lang attibutes of html elements dynamically.

== Description ==

This script allows you to write multi language web pages and simple change between these languages.
All you have do is write all language contents in html and wrap it use span tag with lang attributes(ISO 639-1). and you can call langChange function to change it.

== Usage ==

1. link or copy&paste langChange.js in your html.
2. write your multi language html contents separate in span tag with lang code.
3. hide all contents has lang attribute except your default langauge.
4. add langChange function to onclick events of link button.

###### * you must hide all of other languages block except default language after html loaded.
* call langChange function after html loaded.
```
<html>
<head>
	<script type="text/javascript" src="langChange.js"></script>
</head>
<body>
	<p>
		<span lang=ja>こんいちは。</span>
		<span lang=en>Hello.</span>
		<span lang=zh>您好。</span>
	</p>
  ...
	
	<script type="text/javascript">
		langChange('en');
	</script>
	
</body>
</html>
```
* hide with css.
```
<html>
<head>
	<script type="text/javascript" src="langChange.js"></script>
	<style type="text/css">
    	*[lang=zh] { display : none }
    	*[lang=en] { display : none }
	</style>
</head>
<body>
	<p>
		<span lang=ja>こんいちは。</span>
		<span lang=en>Hello.</span>
		<span lang=zh>您好。</span>
	</p>
  ...
</body>
</html>
```

###### * call langChange function.
```
<a href="#" onclick="langChange('ja');">日本語</a>
<a href="#" onclick="langChange('en');">English</a>
<a href="#" onclick="langChange('zh');">中文</a>
```

== Option ==

langChange function's default changing tag is span. If you want to change other tag you can call function with tag parameter.
```
	<script type="text/javascript">
		langChange('ja','div');
	</script>
```
