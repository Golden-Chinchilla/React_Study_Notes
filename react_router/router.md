## React Router
`https://reactrouter.com/home`

## 前端路由
`path`与`component`的对应，当浏览器中访问不同的`path`，页面就会渲染（切换）不同的`component`（<span style='color:pink'>区别于页面的跳转</span>）

```javascript
const routes = [
    {
        path: './home',
        component: home
    },
    {
        path: './about',
        component: about
    }
]
```