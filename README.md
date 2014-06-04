Junil Um  
http://blog.powerumc.kr

BACKGOUNDS
=========
The jQuery 1.7.1 has bug a few problem. It couldn't compatible Internet Explorer 10. So you has a some bug if you have been used the jQuery 1.7.1 version.

You have to use this jQuery 1.7.1 patch you want to use the jQuery 1.7.1


HOW TO PATCH
============

Following code block has to error on the IE 10 Web Browser.

**Original source block**
```js
2699:	return ( ret.nodeValue = value + "" );
```

**To be patch**
```js
2699:	return ( !$.browser.msie || $.browser.version < 7 ) ? ( ret.nodeValue = value + "" )
                                                            : void(0);
		}
```

SUPPORT
=======
- Fixed : Junil, Um
- Website: http://blog.powerumc.kr
- Contact: powerumc@gmail.com
