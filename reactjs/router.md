* Reactta tek html dosyası üzerinden çok sayfa gösterimi yapılır (Multiple Pages in SPAs) 

* /blog /about /user/1 vs gibi pathler parse edilerek sayfa tekrar render edilir. Bu sayfaların hiçbiri gerçek bir html sayfası değildir.


```javascript
npm install --save react-router-dom
```


* Route componenti çoklanarak hangi pathte ne yapılacağı yazılır. 
  
* **exact** parametresi render methodunun sadece bu pathte çalışmasını sağlar, eğer bu path ile başlayan tüm pathlerde çalışması gerekiyorsa bu parametre kullanılmaz.
  
* Aşağıdaki örnekte / pathinde Home ve Home 2 görünürken /xyz pathinde sadece Home 2 görünür.
  
```javascript
import {Route} from 'react-router-dom';

//...

<Route path="/" exact render={() => <h1>Home</h1>}/>
<Route path="/" render={() => <h1>Home 2</h1>}/>

<Route path="/" exact component={ABCComponent}/>
```

* Eğer pathler `<a>` tagi ile tanmlanırsa browser davranışı sebebiyle sayfe her seferinde komple yenilenir. bu durumun üstesinden gelmek, sadece sayfanın ilgili bölümünün yeniden yüklenmesini sağlamak için router ın `<Link>` componenti kullanılır. 
  

```javascript
import {Route, Link} from 'react-router-dom';

//...

<Link to="/">Home</Link>
```

* Routing propertileri **(history, location, match)** alt komponentlere de taşınmak isteniyorsa **withRouter** HOC(High Order Component) i eklenmesi gerekir.

```javascript
import {withRouter} from 'react-router-dom';

//...

export default withRouter(post);
```
---
**Absolute Path vs Relative Path**

* Absolute path `<Link to="/new" ...` şeklinde tanımladığımız her tıkladığında context pathi replace eden klasik tanımlama şekli `example.com/new ` gibi.
* Relative path ise dinamik oluşturulan ve sonuna eklenerek devam eden url anlamına geliyor. */new*  pathini dinamik olarak sona eklemek istediğimiz durumlarda `<Link to={props.match.url + '/new'}>` şeklinde bir tanımlama yapabiliriz. Bu sayede `example.com/posts/new` ya da `example.com/all-posts/new` şeklinde pathleri de kampsam içine almış oluruz.
* Absolute ya da Relative daha iyidir gibi bir durum yoktur, isteğe ve ihtiyaca bağlı olarak kullanılır.

---

* **NavLink** componenti **Link** gibi çalışır fakat genellikle menü amaçlı kullanılır ve aktif olan menu linkine default olarak **active** classını ekler. Bu sayede seçili menü ile ilgili farklı css yazılabilir. **axact** parametresi active classının sadece seçili olduğu zaman eklenmesi için kullanılır, kullanılmaz ise seçili olmadığında da eklenir. **activeClassName** parametresi opsiyoneldir, yazılmadığında default active classı kullanılır. **activeStyle** parametresiyle de inline style uygulanabilir.

```javascript
<NavLink 
        to="/" 
        exact
        activeClassName="active"
        activeStyle={{
            color: '#fa923f',
            textDecoration: 'underline'
        }}>
    Home
</NavLink>
```
---
**Dinamik Parametre Geçişi**

*Sayfalar arası *id* gibi dinamik parametre geçişleri için,

```javascript
<Route path="/:id" exact component={FullPost} />
```

şeklinde tanımlama yapmak gerekir. Bu sayfaya yapılan yönlendirme linki

```javascript
<Link to={'/' + post.id}>
    <Post
        title={post.title}
        author={post.author}
        clicked={() => this.postSelectedHandler(post.id)} />
</Link>;
```
ya da kodlama ile yönlendirmek yapmak için
```javascript
this.props.history.push({pathname: '/' + id});
//this.props.history.push('/' + id);
```
kullanılabilir.

>***Not:*** *history objesi navigasyon için kullanılır. içinde *go, goBack, goForward, push* gibi fonksiyonlar vardır.*


Parametrelere  ulaşmak için `match.params.paramter_name` kullanılır

```javascript
componentDidMount () {
    if ( this.props.match.params.id ) {
        if ( !this.state.loadedPost 
            || (this.state.loadedPost 
                && this.state.loadedPost.id !== this.props.id) ) {
            
            axios.get( '/posts/' + this.props.match.params.id )
                .then( response => {
                    this.setState({ 
                        loadedPost: response.data 
                    });
                });

        }
    }
}
```

* `?something=somevalue` şeklinde oluşan *query* parametrelerinin oluşturulması ve parse edilmesi;

parametrelerin yollanması
```javascript
<Link to="/my-path?start=5">Go to Start</Link> 
```
ya da
```javascript
<Link 
    to={‌{
        pathname: '/my-path',
        search: '?start=5'
    }}>
    Go to Start
</Link>
```
parametrelerin alınması
```javascript
componentDidMount() {
    const query = new URLSearchParams(this.props.location.search);
    for (let param of query.entries()) {
        console.log(param); // yields ['start', '5']
    }
}
```

* `#something` şeklinde oluşturulan *hash* parametreleri de `props.location.hash` üzerinden alınır;
  
```javascript
<Link to="/my-path#start-position">Go to Start</Link>
```
```javascript
<Link 
    to={‌{
        pathname: '/my-path',
        hash: 'start-position'
    }}
    >Go to Start</Link>
```
---
* `<Switch>` componenti aynı anda tek route un render edilmesini sağlar. Aşağıdaki gibi durumlarda `path="/new-post"` ve `path="/:id"` üstüste bineceğinden, bu durumun önüne geçmek için **switch** kullanılabilir. Seçimi yukarıdan aşağıya doğru yapar.

```javascript
import {Route, NavLink, Switch} from 'react-router-dom';

//...

 <Switch>
    <Route path="/" exact component={Posts} />
    <Route path="/new-post" component={NewPost} />
    <Route path="/:id" exact component={FullPost} />
</Switch>
```

* `<Redirect>` componenti yönlendirme için kullanılır. Url değişir.

```javascript
import {Route, NavLink, Switch, Redirect} from 'react-router-dom';

//...

<Redirect from="/" to="/posts" />
```

* **Redirect** componenti bir işlem sonucunda yapılacak şekilde de kullanılabilir. Örneğin bi statte değişkeninin durumuna göre sayfa yönlendirilebilir.

```javascript
//...

let redirect = null;
if(this.state.submitted){
    redirect = <Redirect to="/posts" />
}
return (
    <div className="NewPost">
        {redirect}
        <h1>Add a Post</h1>

//...
```

>***Not:*** *Redirect yerine daha pratik şekilde state güncelleme anında* ***props.history.replace*** *fonksiyonu da kullanılabilir. replace fonksiyonunun push fonksiyonundan farkı historyi korumamasıdır. push yapıldığında browserda önceki sayfaya dönülebilir ama replacede dönülemez.*

>***Not:*** *Yetkiye sayfaların gizlenmesi ya da açılması, state üzerinde tutulacak bi değişkenle route ların şartlı yazılması ile yapılabilir ya da ilgili sayfanın componentDidMount methodunda yetki olup olmadığı kontrol edilerek redirect yapılabilir.*

---
**Lazy Loading with Suspense**

Routing sırasında her sayfada tüm jacascript tekrar yükleniyor, sadece seçili componentin yüklenmesi isteniyorsa lazy loading yöntemleri kullanılır.

1. yöntemde aşağıdaki gibi oluşturulan *asyncComponent.js* dosyası

```javascript
import React, { Component } from "react"

const asyncComponent = (importComponent) => {
    return class extends Component {
        state = {
            component: null
        }

        componentDidMount () {
            importComponent()
                .then(cmp => {
                    this.setState({
                        component: cmp.default
                    });
                });
        }

        render () {
            const C = this.state.component;

            return C ? <C {...this.props} /> : null;
        }
    }
}

export default asyncComponent;
```

componentin kullanılacağı routing dosyası içinde aşağıdaki şekilde import edilelerek kullanılır.

```javascript
//...

import asyncComponent from '../../hoc/asyncComponent'
const AsyncNewPost = asyncComponent(() => {
    return import('./NewPost/NewPost');
});

//...

<Route path="/new-post" component={AsyncNewPost} />
```

1. yöntemde ise react v16.6 den gelen yeni özellikler ile birlikte aşağıdaki gibi kullanılabilir. Yine bu versiyonla gelen Suspense özelliği ise component yüklenene kadar işlem yapılmasını sağlar. 

```javascript
import React, { Component, Suspense } from 'react';

const Posts = React.lazy(() => import('./containers/Posts'));


<Suspense fallback={<div>Loading...</div>}>
    <Posts />
</Suspense>

```

* Eğer uygulama *example.com* gibi değil de *example.com/myapp* şeklinde bi path altında çalışacaksa bunun reactte tanımlanması gerekir ve aşağıdaki gibi yapılır.
```javascript
<BrowserRouter basename="/myapp">
...
</BrowserRouter>
```

* Son olarak routing yukarıdan aşağıya sırayla çalıştığı için en sonda bir *Not Found Page* bölümü yapmak gerekir çünkü browser her halükarda index.html i açacaktır.

```javascript
<Route render={() => <h1>Not Found</h1>} />
```

* Döküman: https://reacttraining.com/react-router/web/guides/philosophy