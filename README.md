# Typograf-api
Typography of the text using the web service Typograf.ru
## Installation
```
npm install typograf-api
```
# How to use it

```javascript
var Handler = function(text,err)
    {
        document.getElementById('jstypo_text').value= text;// вывод в textarea
        document.getElementById("text").innerHTML = text;
        
        //text = <p>На&nbsp;лесопилку завезли 32&nbsp;м&sup3; леса, из&nbsp;которых 4&nbsp;м&sup3;
        //пустили под распил на&nbsp;25&nbsp;мм доски, длинной по&nbsp;6&nbsp;м.</p>
    }
    var str = document.getElementById('jstypo_text').value;
    //str = 'На лесопилку завезли 32 м3 леса, из которых 4м3 пустили
    //под распил на 25мм доски, длинной по 6м.';
    
    textTypography(str,Handler);

```
In case of an error, the same text will be returned. Information about the error that occurred can be obtained from the second argument of
the handler.
