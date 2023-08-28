# 📪 Property Routes

## User Routes

#### Get A User Property

```
/property/mine
```

Use this Route to Get User Property.

\
You Need to Send the values below in Your request&#x20;

```
_id: userInfo._id
```

You Will Get an Array Of Values Below From Server To Operate in Your App.

```javascript
{
    tag: { type: String, required: true },
    category: { type: String, required: true },
    valuePerShare: { type: String, required: true },
    totalShareAmount: { type: String, required: true },
    totalValue: { type: Number, required: true },

    owner: {
      type: mongoose.Schema.Types.ObjectId,
      ref: "User",
      required: true,
    },
  },
  {
    timestamps: true,
  }
```



#### Get Specific Category of Assets for a User.

```
/property/mine/:slug
```

You Need to Send the values below in Your request&#x20;

```
_id: userInfo._id,
slug: propertySlug
```

You Will Get The Values Below From Server To Operate in Your App.

```javascript
{
    tag: { type: String, required: true },
    category: { type: String, required: true },
    valuePerShare: { type: String, required: true },
    totalShareAmount: { type: String, required: true },
    totalValue: { type: Number, required: true },

    owner: {
      type: mongoose.Schema.Types.ObjectId,
      ref: "User",
      required: true,
    },
  },
  {
    timestamps: true,
  }
```

#### Route to Create New Asset For A User

```
/property/create
```

Send a Request , Axios For Example , &#x20;

```javascript
axios.post(
        "/property/create",
        {
          tag: values.name,
          category: values.propertyType,
          valuePerShare: values.value,
          totalShareAmount: values.totalShareAmount,
          owner: userInfo._id,
        },
        {
          headers: { Authorization: `Bearer ${userInfo.token}` },
        }
      );
```

#### Route To Edit Specific Property for A user

```
/property/:id
```

Use Axios Example Below to Send the Required Data To Server.

```javascript
axios.put(
        `/property/${id}`,
        {
          _id: id,
          valuePerShare: values.value,
          totalShareAmount: fvalues.totalShareAmount,
        },
        {
          headers: { Authorization: `Bearer ${userInfo.token}` },
        }
      );
```

#### Route To Delete Specific Property for A user

Use Axios Example Below to Delete a Property From Database For an Authenticated User.

```javascript
axios.delete(`/property/${id}`, {
          headers: { Authorization: `Bearer ${userInfo.token}` },
        });
```
