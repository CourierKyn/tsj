# tsj

`tsj` (Tab-seperated JSONs) is a simple text format just like `tsv`, but more robust and elegant!

- Each value is JSON-serialized, and that includes any naughty strings containing `\n`, `\t` or even any data structure.

- Tab seperated, super easy to edit and read by humans.

- No more quoting character like `"`, `""`, `""""`. I hate double quoting!

- Hand coded loading and writing function, easy to handle by yourself.

------------

Super easy example in Python:

```python
header = ('index', 'a', 'b', 'c')
data = [[0, 'hello', 'world', 42],
         1, 'llo\r\nhe', 'ld\twor', 24],
         ...]

for row in header, *data:
    writer.write('\t'.join(map(json.dumps, row)) + '\n')
```

It just works.
