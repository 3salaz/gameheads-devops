# Hello, Testing 1,2,3

Testing out some plugin down below, will be adding more soon that we can use within the lessons

> [!NOTE]
> An alert of type 'note' using global style 'callout'.

> [!TIP]
> An alert of type 'note' using global style 'callout'.

> [!WARNING]
> An alert of type 'note' using global style 'callout'.

> [!ATTENTION]
> An alert of type 'note' using global style 'callout'.

## Tabs 
<!-- tabs:start -->

#### **English**

Hello!

#### **Spanish**

Hola!

#### **Italian**

Ciao!

<!-- tabs:end -->

```javascript
const a = 1;
const b = 2;
const c = 3;
```

<div id="gitalk-container"></div>


<script>
    const gitalk = new Gitalk({
        clientID: 'GitHub Application Client ID',
        clientSecret: 'GitHub Application Client Secret',
        repo: 'GitHub repo',      // The repository of store comments,
        owner: 'GitHub repo owner',
        admin: ['GitHub repo owner and collaborators, only these guys can initialize github issues'],
        id: location.pathname,      // Ensure uniqueness and length less than 50
        distractionFreeMode: false  // Facebook-like distraction free mode
})

gitalk.render('gitalk-container')
</script>