# Introduction

Welcome to the mdBook docs site.

This is a Ruby snippet:

```ruby
module Enumerable
  def uniq
    result = []
    uniq_map = {}
    if block_given?
      each do |value|
        key = yield value
        next if uniq_map.has_key?(key)
        uniq_map[key] = true
        result << value
      end
    else
      each do |value|
        next if uniq_map.has_key?(value)
        uniq_map[value] = true
        result << value
      end
    end
    result
  end
end
```
