# Rename files in a folder with Ruby

If you want to rename files in a folder with Ruby use this script:

```ruby
require 'fileutils'

dir = "/path/to/directory"

Dir.foreach(dir) do |file|
  next if file == '.' or file == '..'

  if !file.include? "string_to_match"
    next
  end

  old_name = "#{dir}/#{file}"
  new_name = old_name.sub("string_to_match", "string_replace")
  FileUtils.mv(old_name, new_name)
end
```

And Done!!!