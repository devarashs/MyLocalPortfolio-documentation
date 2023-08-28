# 📪 User Routes

## User Routes

#### Sign in Route

<pre><code><strong>/users/signin
</strong></code></pre>

Use this Route to Authenticate the users.

\
You Need to Send the values below in Your request&#x20;

```
name: user.name,
email: user.email,
password: user.password,
preferredCurrency: user.preferredCurrency,
```

You Will Get The Values Below From Server To Operate in Your App.

```
_id,
name,
emaill,
preferredCurrency,
isAdmin,
token,
```



#### Sign Up Route

```
/users/signup
```

You Need to Send the values below in Your request&#x20;

```
name: user.name,
email: user.email,
password: user.password,
preferredCurrency: user.preferredCurrency,
```

You Will Get The Values Below From Server To Operate in Your App.

```
_id,
name,
emaill,
preferredCurrency,
isAdmin,
token,
```

#### User Delete Route

```
/users/:id
```

Send the Value below from userInfo Below tho this route to delete an Only Authenticated and None Admin User

```
id: userInfo._id,
```

#### Update User Info route

```
/users/profile/:id
```

You Can change values below by simply sending an id , a type of info you want to change (name,email,password) and a the new value

```
{
    id: userInfo._id
    type: name||email||password
    value: someValue
}
```
