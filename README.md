# LinkedIn-Scraping
Random snippets for getting data from LinkedIn

Scroll to bottom
```
for (var i = 0; i < 4000; i++) {
    setTimeout(function() {
	window.scrollTo(0,document.body.scrollHeight);
    }, 500 * i);
}
```

Get all people elements
```
const elements = document.getElementsByClassName('pr4 artdeco-entity-lockup artdeco-entity-lockup--size-4 ember-view')

var cleaned = []
Array.from(elements).forEach(element => {
    name = element.getElementsByClassName('artdeco-entity-lockup__title ember-view')[0].innerText
    job = element.getElementsByClassName('artdeco-entity-lockup__subtitle ember-view')[0].innerText
    cleaned.push({'name': name, 'job': job})
});

var json = JSON.stringify(cleaned);
```


