# React Router の検証用のリポジトリ

## react Router でどう型安全に作るか

### 問題点
```
<Switch>
    <Route path="/home">
        <Home>
    </Route>
    <Route path="/login">
        <Login>
    </Route>
    <Route path="/user/:id">
        <User>
    </Route>
</Switch>
```


```
const {id} = useParams<{id:string}>();
```
と言う形で型定義できるが、型安全とは言い難い。