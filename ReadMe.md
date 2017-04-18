# Ci Programming Language & `Cito` Tool

**Ci** is automatically translated language, aimed at crafting **portable programming libraries**, with syntax akin to C#.

`cito` tool automatically translates the Ci programming language to C, Java, C#, JavaScript, ActionScript, Perl and D.

The translated code is lightweight (no virtual machine, emulation or large runtime), human-readable and fits well the target language (including naming conventions and documentation comments).

Current version of Ci doesn't support standalone programs or even console output,
so your **"Hello world"** could be the following library:

```cs
public class HelloCi {
    public static string GetMessage() {
        return "Hello, world!";
    }
}
```

See [hello.ci](docs/hello.ci) for a slightly bigger example.

# How to install

`cito` is written in C#.

On Windows you need .NET Framework 3.5.
[Download cito binaries](http://sourceforge.net/projects/cito/files/cito/0.4.0/cito-0.4.0-bin.zip/download)
and extract `cito.exe` to a directory in your `PATH` environment variable.

On other platforms install [Mono](http://www.mono-project.com). Mono runs .NET executables:

```
mono cito.exe
```

For your convenience, create Mono wrapper scripts such as:

```
#!/bin/sh
exec /usr/bin/mono /usr/local/lib/cito/cito.exe "$@"
```

so that you can type `cito` instead of `mono cito.exe`.

# How to use

Call `cito` from command prompt passing source files (with the extension `.ci`) and one of the destination files
(its filename extension determines the target language), for example:

```
cito -o hello.c hello.ci
cito -o HelloCi.java hello.ci
```

`cito` only generates source code. It is your responsibility to compile it.

# History

### (2017-04-18)

- Fork on GitHub for future development

### cito 0.4.0 (2013-05-18)

- Perl 5 back-end.
- Dynamic object allocation.
- `default` clause must be the last in `switch`.
- String concatenation in D.
- Java fix for code such as `cond ? 1 : 0`.
- C fix for code such as `if (cond) methodThatThrows(); else stmt();`
- `cipad` opens files, has font selection and improved UI.

### cito 0.3.0 (2013-02-15)

- Class inheritance with virtual methods.
- Dynamic array allocation.
- Extended constant folding.
- JavaScript Typed Arrays.
- Installs Mono wrappers for `cito` and `cipad`.

### cito 0.2.0 (2011-08-03)

- Created `cipad` - a simple Ć editor with on-the-fly translation.
- Changed syntax of arrays of storage: `MyClass[]()` -> `MyClass()[]`, `string[](8)` -> `string(8)[]`.
- Fixes for the `byte` type in ActionScript and C#.
- String comparisons in C and Java.
- Fixed translation of delegates to C in `cito` compiled on .NET < 4.
- Fixed errors with the new and 64-bit D compilers.
- Some optimizations for string handling in C.
- Documentation translated to English.

### cito 0.1.0 (2011-05-24)

- Initial release.

# Authors
- Piotr Fusik (Ci and cito)
- Adrian Matoga (D back-end)

