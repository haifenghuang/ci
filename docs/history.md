current:
- @ is short for one line native. For example `@printf("Hello world");`
- Fork on GitHub for future development (2017-04-18)

cito 0.4.0 (2013-05-18):
- Perl 5 back-end.
- Dynamic object allocation.
- `default` clause must be the last in `switch`.
- String concatenation in D.
- Java fix for code such as `cond ? 1 : 0`.
- C fix for code such as `if (cond) methodThatThrows(); else stmt();`
- `cipad` opens files, has font selection and improved UI.

cito 0.3.0 (2013-02-15):
- Class inheritance with virtual methods.
- Dynamic array allocation.
- Extended constant folding.
- JavaScript Typed Arrays.
- Installs Mono wrappers for `cito` and `cipad`.

cito 0.2.0 (2011-08-03):
- Created `cipad` - a simple Ć editor with on-the-fly translation.
- Changed syntax of arrays of storage: `MyClass[]()` -> `MyClass()[]`, `string[](8)` -> `string(8)[]`.
- Fixes for the `byte` type in ActionScript and C#.
- String comparisons in C and Java.
- Fixed translation of delegates to C in `cito` compiled on .NET < 4.
- Fixed errors with the new and 64-bit D compilers.
- Some optimizations for string handling in C.
- Documentation translated to English.

cito 0.1.0 (2011-05-24):
- Initial release. 
