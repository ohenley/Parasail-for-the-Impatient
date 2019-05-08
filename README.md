# ParaSail for the Impatient

## To whom? Awww you can skip this section...

- You like to test drive everything right away? 
- You just got some headlines about ParaSail and ... OMG, I need to try it Right-F....-Now! 
- Reference manuals gives you restless legs syndrome? 
- You are not afraid to have your hands dirty?
- More often than not you like brain dead instructions
- You ride a bike without a helmet...

You are like me, an impatient.


## Why would it interest me? Awww skip too...

"ParaSail" stands for Parallel, Specification and Implementation Language. 
* Created by by S. Tucker Taft, on of the main deisgner of Ada95 and upward. 

- Is an object-oriented parallel programming language.
- Provides support for both implicit and explicit parallelism.
- Can be mapped to multicore, many core, heterogeneous, or distributed architectures.
- Uses a pointer-free programming model, where objects can grow and shrink, and value semantics are used for assignment. 
- Has no global garbage collected heap. Instead, region-based memory management is used throughout. 
- Includes the following high-level specification features:
  - parameterized modules with full separation of interface from implementation 
  - pre- and post-conditions for individual operations within a module 
  - invariants that apply across all operations within a module
  - constraints that apply to individual instances of a module
- Types can be recursive, so long as the recursive components are declared optional. 
- Subtyping 'ala' Ada is core.
- There are no global variables, no parameter aliasing, and all subexpressions of an expression can be evaluated in parallel. 
- Assertions, preconditions, postconditions, class invariants, etc., are part of the standard syntax, using a Hoare-like notation. 
- Any possible race conditions are detected at compile time.
- Both an interpreter using the ParaSail virtual machine, and an LLVM-based ParaSail compiler are available. (Linux, Windows, MacOS)
- Work stealing is used for scheduling ParaSail's light-weight threads.
- Can interface Ada and C.

Pretentious but important note: if the previous points do not convince you to try ParaSail it is probably because you do not understand their implications for the craft of programming or you are just born stupid. The only thing I can tell you is that you will inevitably care one day or another under one form or another. Better save you the trouble right away...  

## Preparation

### Windows

- If not done already, download [ParaSail](https://drive.google.com/file/d/1h6FiwuZU9PoNFEp5a3Lp4C-6YG121w_n/view).
- Unzip it somewhere on your file system.
- Add the following path "/where-you-just-unzipped-ParaSail/parasail_release_8_0/\_win" to your system environment variables. Note: On windows, adding these variables sucks big time, so I recommend downloading and installing [Rapid Environment Editor: REE](https://www.rapidee.com/en/download). Once installed open it and append "/where-you-just-unzipped-ParaSail/parasail_release_8_0/\_win" to the "Path" variable (either System Variables or User Variables will make it). You can thank me later for REE...
- Open a command prompt inside the folder "/where-you-just-unzipped-ParaSail/parasail_release_8_0/examples"

### Not Hello World ...
Copy and paste this line at the cmd:
```
parasail_main.exe fib.psl "../lib/aaa.psi"
```
If everything goes well the REPL should give you this:

```
Command to execute:
```
Now enter ```diff Fib 8```

```
Result :  21
Command to execute: 
```
Now enter:
```
main 8
```
```
Fib(8) = 21
Command to execute: 
```
Now enter:
```
main 7 9
```
```
Fib(7) = 13
Fib(9) = 34
Command to execute:
```

Now open fib.psl in your prefered text editor and study it. IF you already programmed and know about the classic recursive Fibonaci method you should understand most of the code right away even without prior ParaSail training.


