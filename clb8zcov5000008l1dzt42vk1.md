# How use composition in rails

In Ruby on Rails, composition is a technique for structuring your application by combining small, independent modules (or "concerns") into larger, cohesive classes. This allows you to reuse code and keep your application organized and maintainable.

Here is an example of how you might use composition in a Rails application:

```ruby
# app/models/user.rb
class User < ApplicationRecord
  include UserAuthentication
  include UserProfile
  include UserPermissions
end

# app/models/concerns/user_authentication.rb
module UserAuthentication
  extend ActiveSupport::Concern

  included do
    has_secure_password
    validates :email, presence: true, uniqueness: true
  end

  def authenticate(password)
    # Check if the given password is correct
  end

  def generate_password_reset_token
    # Generate a password reset token
  end
end

# app/models/concerns/user_profile.rb
module UserProfile
  extend ActiveSupport::Concern

  included do
    validates :name, presence: true
  end

  def full_name
    # Return the user's full name
  end

  def update_name(new_name)
    # Update the user's name
  end
end

# app/models/concerns/user_permissions.rb
module UserPermissions
  extend ActiveSupport::Concern

  included do
    # Define permissions for the user
  end

  def can_edit_posts?
    # Check if the user has permission to edit posts
  end

  def can_delete_comments?
    # Check if the user has permission to delete comments
  end
end
```

In this example, the `User` model is composed of three concerns: `UserAuthentication`, `UserProfile`, and `UserPermissions`. Each concern defines a set of related methods and validations, and the `User` model includes all three concerns to provide a complete, cohesive set of functionality.

By using composition in this way, you can keep your code organized and avoid creating large, monolithic classes that are difficult to maintain and test. It also allows you to easily reuse code across multiple models, and make your application more modular and flexible.