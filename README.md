# cool-php-captcha
This is the official GitHub project from code.google.com/p/cool-php-captcha



This project generates friendly captcha images. This project provides the SimpleCaptcha class.
Some fetures are: Background and foreground colors, dictionary words, non-dictionary random words, blur, shadows, JPEG and PNG support.


Basic example
-------------


```php
session_start();
$captcha = new SimpleCaptcha('captcha_name');
// Change configuration...
//$captcha->wordsFile = null;           // Disable dictionary words and use random letters instead
//$captcha->wordsFile = 'words/es.txt'; // Enable spanish words dictionary
//$captcha->session_var = 'secretword'; // Changes the session variable from 'captcha' to 'secretword'
$captcha->CreateImage();
```

... will output an image, for example:
<br>
![http://cool-php-captcha.googlecode.com/files/example.jpg](http://cool-php-captcha.googlecode.com/files/example.jpg)



You can validate the php captcha with: (case-insensitive version)

```php
$captcha = new SimpleCaptcha('captcha_name');
if( $captcha->check($_REQUEST['captcha_val']) )
  return "Invalid captcha";
}
else {
  // process request
}
```

You can see a live example here: http://joserodriguez.cl/cool-php-captcha


More examples
-------------
Background and foreground colors, dictionary words, non-dictionary random words, blur, shadows, JPEG and PNG support:<br>
<br>
<img src='http://cool-php-captcha.googlecode.com/files/examples.jpg' />



