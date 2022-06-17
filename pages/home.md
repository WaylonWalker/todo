---
title: home
uuid: ff37bdd1-e01b-4dc2-b4d7-02e4378f5456
---

<style>
body {
max-width: none;
padding: 1rem;
}
.wrapper {
    display: flex;
    flex-direction: row;
}
.wrapper ul{
list-style-type: none;
}

li {
background: rgba(255, 255, 255, .1);
margin: 1rem;
padding: .2rem;
border-radius: 5px;
}
.section {
    flex: 1 1 300px;
    display: flex;
    flex-direction: column;
}
</style>


<div class='wrapper'>

<div class='section'>
<h2>
todo
</h2>
<ul>
{{ '\n'.join(markata.map('f"<li> <a href=\'/{slug}\' title=\'{title}\'>{title}</a> <br> {content}</li>"', sort='slug', filter='status=="todo"')) }}
</ul>
</div>

<div class='section'>
<h2>
doing
</h2> <ul>
{{ '\n'.join(markata.map('f"<li> <a href=\'/{slug}\' title=\'{title}\'>{title}</a> <br> {content}</li>"', sort='slug', filter='status=="doing"')) }}
</ul>
</div>

<div class='section'>
<h2>
done
</h2>
<ul>
{{ '\n'.join(markata.map('f"<li> <a href=\'/{slug}\' title=\'{title}\'>{title}</a> <br> {content}</li>"', sort='slug', filter='status=="done"')) }}
</ul>
</div>
</div>
