# About me #
**Fullname:** Dmitry Muzychenko

**Date of birth:** 07/07/2001

**Location:** Belarus, Minsk

**English level:** B1

**Education:** General secondary education

# Contacts #
[Telegram](t.me/dmdevel)

[Facebook](https://web.facebook.com/profile.php?id=100012758914011)

nogrevonlight@gmail.com

# Goals #
I'm a junior web developer. I want to get team development experience and I always like to learn something new for extending my knowledges. It's easy for me to contact with new people. Also I can say that I'm 
easily trained. I made a lot of projects for myself (which will never be released), and some for another people.

# Skills #
* Vue.js (+Vue Router)
* Axios
* native JavaScript
* jQuery
* HTML5, CSS3
* Node.js (+express)
* MySql
* MongoDB
* nginx
* Git

# Code examples #
Method for sending POST requests to the server (link shortener) with using `Vue` and `Axios`
```JavaScript
makeShortRequest: function() {
  if(this.link.trim()) {
    let queryAddress = location.href + "generate?link=" + this.link;
    let resultFunc = function(response) {
      console.log(response);
      let temp = localStorage.links ? JSON.parse(localStorage.links) : {};
      temp[response.data] = this.link;
      localStorage.links = JSON.stringify(temp);
      this.$root.$emit('openModal');
    }
    Axios.post(queryAddress).then(resultFunc.bind(this));
  }
}
```
Method for Node.js application which checks is url exists 
```JavaScript
app.get('/:link', (req, res) => {
  database.collection('links').findOne({ 'short_link': req.params.link }, (err, data) => {
    if(err) {
      throw err;
    }
    res.redirect(data['original_link']);
  });
})
```

# Experience #
Online shop "Belarusachka" [[Link]](https://www.belarusachka.by/en/)

Stack: 
* jQuery
* native JavaScript
* HTML5, CSS3

Link shortener "Shlink" [[Source]](https://github.com/musicchenko/shlink)

Stack:
* Vue.js (+Vue Router)
* Node.js (+express)
* MongoDB
* HTML5, CSS3
