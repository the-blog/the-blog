exit.rb
```ruby
def exit_command?(cmd)
  %w[ exit quit ].include?(cmd.downcase)
end

def exit_instruction
  puts "for Exit write `exit` or `quit`"
end
```

main.rb
```ruby
require_relative 'exit'

exit_instruction

loop do
  puts "Hello! Insert the command"
  cmd = STDIN.gets.chomp
  exit_command?(cmd) && break
end
```
