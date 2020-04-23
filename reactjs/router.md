* Reactta tek html dosyası üzerinden çok sayfa gösterimi yapılır (Multiple Pages in SPAs) 

* /blog /about /user/1 vs gibi pathler parse edilerek sayfa tekrar render edilir. Bu sayfaların hiçbiri gerçek bir html sayfası değildir.


```
npm install --save react-router-dom
```


* Route componenti çoklanarak hangi pathte ne yapılacağı yazılır. 
  
* **exact** parametresi render methodunun sadece bu pathte çalışmasını sağlar, eğer bu path ile başlayan tüm pathlerde çalışması gerekiyorsa bu parametre kullanılmaz.
  
* Aşağıdaki örnekte / pathinde Home ve Home 2 görünürken /xyz pathinde sadece Home 2 görünür.
  
```
import {Route} from 'react-router-dom';

...

<Route path="/" exact render={() => <h1>Home</h1>}/>
<Route path="/" render={() => <h1>Home 2</h1>}/>

<Route path="/" exact component={ABCComponent}/>
```

* Eğer pathler `<a>` tagi ile tanmlanırsa browser davranışı sebebiyle sayfe her seferinde komple yenilenir. bu durumun üstesinden gelmek, sadece sayfanın ilgili bölümünün yeniden yüklenmesini sağlamak için router ın `<Link>` componenti kullanılır. 
  

```
import {Route, Link} from 'react-router-dom';

...

<Link to="/">Home</Link>
```

* Routing propertileri **(history, location, match)** alt komponentlere de taşınmak isteniyorsa **withRouter** HOC(High Order Component) i eklenmesi gerekir.

```
import {withRouter} from 'react-router-dom';

...

export default withRouter(post);
```
---
**Absolute Path vs Relative Path**

* Absolute path `<Link to="/new" ...` şeklinde tanımladığımız her tıkladığında context pathi replace eden klasik tanımlama şekli `example.com/new ` gibi.
* Relative path ise dinamik oluşturulan ve sonuna eklenerek devam eden url anlamına geliyor. */new*  pathini dinamik olarak sona eklemek istediğimiz durumlarda `<Link to={props.match.url + '/new'}>` şeklinde bir tanımlama yapabiliriz. Bu sayede `example.com/posts/new` ya da `example.com/all-posts/new` şeklinde pathleri de kampsam içine almış oluruz.
* Absolute ya da Relative daha iyidir gibi bir durum yoktur, isteğe ve ihtiyaca bağlı olarak kullanılır.

---

* **NavLink** componenti **Link** gibi çalışır fakat genellikle menü amaçlı kullanılır ve aktif olan menu linkine default olarak **active** classını ekler. Bu sayede seçili menü ile ilgili farklı css yazılabilir. **axact** parametresi active classının sadece seçili olduğu zaman eklenmesi için kullanılır, kullanılmaz ise seçili olmadığında da eklenir. **activeClassName** parametresi opsiyoneldir, yazılmadığında default active classı kullanılır. **activeStyle** parametresiyle de inline style uygulanabilir.

```
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
