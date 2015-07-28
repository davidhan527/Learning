# Escaping HTML in ERB

- If you do not mark a string as `html_safe` in ERB, by default checks if a string is html_safe and if it is not, it will encode the unsafe values and then mark it as html_safe.
- If you mark a string as `html_safe` and then append to it, the appended string will be automatically encoded and marked as html_safe.

```ruby
# Rails -v 3.2.22

html = "string".html_safe + "<script>" // "string&lt;script&gt;"
html.html_safe? // true
```

- You can encode string by:

```ruby
HTMLEntities.new.encode("<script>").html_safe
```
