Review - http://thesagittariusme.blogspot.com/2016/12/js30-challenge-day1-js-drum-kit.html

Reminded me of putting the following in every project
```
<html lang="en-US">
<meta charset="UTF-8">
```

and optionally
```
<meta name="author" content="Arjun Khode">
```

- We can find the keyCode of each key on the site keycode.info

What <kbd> does
The HTML Keyboard Input Element <kbd> represents user input and produces an inline element displayed in the browser's default monospace font.

```
window.addEventListener(‘keydown’, function(e){}) //note keydown is in quotes. And it is window, not document.
```

```
audio[data-key=“{e.key}”]` //where data-key has to have its value in double quotes, the whole querySelector expression has to be in back ticks (`) for template literal notation and the value is a variable inside the event e, which is called keyCode, a property of event 'e'.
```