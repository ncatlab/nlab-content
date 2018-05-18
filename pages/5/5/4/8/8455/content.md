
A [[logical framework]].

## Related concepts

* [[Automath]]

* [[Elf]]

## References

* [Twelf homepage](http://twelf.org/wiki/Main_Page)

## Installation notes

The precompiled binaries available on the [Twelf download page](http://twelf.org/wiki/Download) are for rather old machines.  However, it appears that they can still be run on modern machines as long as the relevant 32-bit libraries are present and have the expected names.  On Ubuntu 18.04 the following sequence of commands sufficed for at least one person to be able to run the Twelf binaries:

```
sudo dpkg --add-architecture i386
sudo apt install libgmp10:i386
sudo ln -s /usr/lib/i386-linux-gnu/libgmp.so.10 /usr/lib/i386-linux-gnu/libgmp.so.3
```


category: software
