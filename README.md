### Sorcery
---

https://github.com/Sorcery/sorcery

```sh
gem 'sorcery'
bundle
gem install sorcery
rails g sorcery:install
rails g sorcery:install remember_me reset_password
rails g sorcery:install --model Person
rails g sorcery:install http_basic_auth external remember_me --only-submodules
```

```ruby
require_login
login(email, password, remember_me = false)
auto_login(user)
logout
logged_in?
current_user
redirect_back_or_to
@user.external?
@user.active_for_authentication?
@user.valid_password?('secret')
User.authenticates_with_sorcery!

require_login_from_http_basic

login_at(provider)
login_from(provider)
create_from(provider)
build_from(provider)

auto_login(user, should_remember = false)
remember_me!
forget_me!
force_forget_me!

User.load_from_reset_password_token(token)
@user.generate_reset_paswword_token!
@user.deliver_reset_password_instructions!
@user.change_password!(new_password)

invalidate_active_sessions!

User.load_form_activation_token(token)
@user.setup_activation
@user.activate!


```

