# Triode
An emulator for ternary computing.

This has been archived because I'm rewriting it in Rust. I wrote this in C++ originally to revisit it and learn new features and etc for a class i'm taking. 

See the new version here soon: https://github.com/Jviguy/Triode

## Warning small rant of my recent coding experience:

After writing this I remembered why I don't really like C/C++ memory safety and implicit being the default. I mean overally really cool language and after a while I can understand memory aspects better. 
But along with that I can see how stupid some of this stuff is. Copy constructors move constructors, the ownership model not really existing but hey smart points do it. With a good amount of invariance not being guaranteed.
A lot of language features that feel added in just to add some convience but still fit into legacy requirements and not interrupt those. Like the initialization list, you can't reuse calculations in it. Mind you these methods are the only way
to prevent the default constructors from being called on your objects. Every allocation of a new object takes basically two initializations depending on if you can use init lists or not. Its a good language and has its place
but like when there exists a better way why not do it.

As to why I think Rust solve those problems. Different paradigms and isn't covering legacy code from 20 years ago. Memory management is very explicit and that may seem bad to many but I think once you understand the real cost of copying memory.
It makes more sense that way. Like advanced C++ you have to just know that hey yeah if I dont const reference that vector or whatever, it will just copy that entire vector. Like you already have to think of these things.
Why not have the compiler tell you it lol. it just doesn't make sense to me. The way that Rust code is wrote can be weird at some point. In my opinion there is some things like proc macros which I dont really appreciate.
Like I would like to just read a packages code and then its just a file of like 3 proc macros that are complex as hell and then like only a small bit of real code that uses the macros. 
Some people see it as a circle jerk look at my cool trick and etc. But im trying to move towards making sure all my code is tested, working, and understandable. Because it just isn't helpful for me to have to read 5 proc macros
to know what code does lol. I've also seen the argument against rust like developer productivity is bad and slower. But I think the real reason of that is lack of experience with the language and not being used to having these things explicit.
Also just a entire misunderstanding of memory management / Data oriented design, your code and abstractions really don't matter. If the code is fastest on the CPU thats what matters to me. Now I have a limit to that I think manually doing assembly and etc inlining or whatever is too much. Stick by your languages rules.
If you need that speed write the whole damn thing in assembly lol. I think by going and suffering through the Rust learning curve and etc for your period of bad productivity is literally just learning a new look at programming and a computer.
That we just don't normally have when coding.

As such im sticking to Rust for personal projects for now I think. If im going to write something for myself I want to do it in what I believe to be the most high quality.


