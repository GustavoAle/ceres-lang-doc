# Examples

### Hello world
Since the S3MC processor currently run on a FPGA the basic input and output is
given by the serial port.
```c
#extern {
    "serial.cr"
}

sub main()
{
    /*init serial with 115200 bps*/
    IO.init(115200)

    IO.print("hello world\n")
}
```


### Fibonacci
```c
...

fun fib(n)
{
    if(n == 1 or n == 2)
    {
        return 1
    }
    return fib(n-1)+fib(n-2)
}

...
```
