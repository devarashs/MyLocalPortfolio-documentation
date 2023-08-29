# 🔗 Property Data Model

Data Models are Built using Mongoose Data Schema For MongoDB Database Below You See The Model That is Shaping User in the Database\


```javascript
import mongoose from "mongoose";

const propertySchema = new mongoose.Schema(
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
);

const Property = mongoose.model("Property", propertySchema);
export default Property;

```
