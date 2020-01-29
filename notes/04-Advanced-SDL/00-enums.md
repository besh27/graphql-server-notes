# Enums

- A set of discrete values that can be used in place of Scalars
- An enum field must resolve to one of the values in the Enum.
- Great for limiting a filed to only a few different options.

in schema.js

```javascript
enum PetType {
    Dog
    Cat
    Mouse
    Gerble
}
```

next you can add this enum to the Pets

```javascript
type Pet{
        id: String!
        createdAt: String!
        name: String!
        type: PetType
    }

input PetInput {
    name: String
    type: PetType
    id: ID
}

```

When working in the GRaphQL playground, this will give you a dropdown of values when writing queries.

BONUS!

```javascript
"""
This text will be displayed in the playgroup over this enum as a description!
"""

enum PetType {
    Dog
    Cat
    Mouse
    Gerble
}
```

## Next Steps

Move on to the next section about [Advanced SDL](../04-Advanced-SDL/01-interfaces.md)
