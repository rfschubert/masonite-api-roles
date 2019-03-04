# masonite-api-roles

Ok guys! Talking with Joseph, the mantainer of [Masonite](https://github.com/MasoniteFramework/) about `scopes` on `Masonite API` package, I just realized that `scopes` are different of `roles`.

They will work together but they are different.

So, I will need build a new package to Masonite to be able to add `User roles` to my `API endpoints`.

**Problems that I want to solve with this new package**
* Some users may have `read only access` to some endpoints
* Some users will have access to more or less fields based on Its `role` and then the correct `scope` will be selected to filter those `sensitive` data

I'm looking for ideas and other problems that you all may have and then I'll start a new open source Masonite Package.

Feel free to add issues and pull requests! Even if you think you have low experience! So we can build something cool and good to every one!

**First ideas**
* Add a column to my `User` model with `roles` to set what `roles` that user has access
* `roles` may be inherited, something like `user: ['read', 'create']` and `admin: ['user', 'delete']` - not exactly this way, but you got the idea
* Be able to add a default `role` to all users

This package will be something like an `ACL` to users, but it should not be so overcomplicated. I want to build something simple and ready to use.
