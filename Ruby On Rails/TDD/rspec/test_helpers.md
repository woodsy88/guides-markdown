```require ‘rails_helper'``` gives us an access to all testing configurations and methods. ```:type => :helper``` treats our tests as helper specs and provides us with specific methods.

```ruby
require 'rails_helper'

RSpec.describe NavigationHelper, :type => :helper do
  
end

```