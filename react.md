## 1. “Switch is not exported from react-router-dom”

这个问题是因为在路由组件中使用了Switch

原因在 react-router-dom 6.0以后 Switch 就 弃用了

现在要用Routes

```react
   <Routes>
        <Route path="/" exact element={<AllMeetupsPage />}></Route>
        <Route path="/favorites" element={<FavoritesPage />}></Route>
        <Route path="/new-meetup" element={<NewMeetupPage />}></Route>
   </Routes>
```

