# How To Get Current User ID In Laravel
The answer: using the Auth facade.

When Laravel is configured with authentication, the Auth facade becomes useful for actions like grabbing the current logged in user id. Auth comes with various methods, one of which is the id() method, and this is where we can grab the authenticated users’ information.

Use the following steps to get the ID of the current logged in user.

# Step 1
Define the Auth facade for usage.
```php
use Illuminate\Support\Facades\Auth;
```
# Step 2
In a controller or similar, utilize the id() method of the Auth facade.

Note: At this point, the user must be already authenticated, if there is a possibility of the user not being authenticated, then please use the Auth::check() method to prevent exceptions being thrown.

Use the following code to populate the $id variable with the logged-in user ID.
```php
$id = Auth::id(); 
```
And that is it, for this example, my user ID is 1, so the value of $id will now return 1.
