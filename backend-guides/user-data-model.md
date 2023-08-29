# 🔗 User Data Model

Data Models are Built using Mongoose Data Schema For MongoDB Database Below You See The Model That is Shaping Property in the Database\


```javascript
import mongoose from "mongoose";

const userSchema = new mongoose.Schema(
  {
    name: { type: String, required: true },
    email: { type: String, required: true, unique: true },
    preferredCurrency: { type: String, required: true },
    password: { type: String, required: true },
    isAdmin: { type: Boolean, default: false, required: true },
  },
  {
    timestamps: true,
  }
);

const User = mongoose.model("User", userSchema);
export default User;

```
