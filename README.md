# Headache

This is a compiler that turns .hdac files into brainfuck code


## Info

Headache is not only a compiler for brainfuck, its also a custom flavour of brainfuck.

Headache supports all the basic brainfuck commands, but also has some extra commands that are unique to Headache.

### New commands

- `$` : Put the current pointer position into memory
- `^` : Set the current pointer position to the current memory value
- `@` : Reset the current pointer position to 0
- `!` : Jump back to the location of the last `^` or `@` command

## Memory layout

The memory layout is as follows:

```txt
1 - 5 : temp data (registers)
6     : number of variables
> 6   : variable jump table -> indexes into variable data
```
