# Optimization - C++

This file will showcase the different optimizations of code in the C++ Language.  
The different optmization points will have different tags to track which type of optmization it is.

## Table of Contents

## Everything as a reference - speed & memory

When possible, it is best to use a reference when passing parameters in methods. This happens in the method declaration.

`void example(int arg1, int arg2)` => `void example(int& arg1, int& arg2)`

Here's the logic. When not passing a variable as a reference, the variable is copied for the method. This takes up time and space on the stack. When instead passing the variable as a reference to it, you are essentially passing the memory address of the variable instead of a copy of the variable. This means that whatever the method does with the variable, it is doing it with the original variable. As you can imagine, this bypasses the copying which saves time and this avoids a duplicate variable which saves space.
