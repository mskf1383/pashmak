# Include scripts
you can distribute your code in more than 1 files.

for example, we have 2 files: `app.pashm`, `fib.pashm`.
`app.pashm` is main file. `fib.pashm` contains a function to show fibonaccy algo.

###### fib.pashm:
```bash
func fib;
    $a = 1;
    $b = 1;

    loop;
        println $b;

        $tmp_a = $a;
        $tmp_b = $b;

        $a = $tmp_b;

        $b = $tmp_a + $tmp_b;
    while $b < 10000;
endfunc;
```

###### app.pashm:
```bash
mem 'fib.pashm'; include ^;

fib;
```

when we run `include` command and pass a file path from mem (^) or variable to that, content of thet file will include in our code and will run. for example, here we used a function from the `fib.pashm` file.

also you can use `import` function to have easier syntax:

```bash
# you can pass value directly to this
import 'fib.pashm';

fib;
```

this is very useful.
