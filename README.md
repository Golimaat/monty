<h1>0x19. C - Stacks, Queues - LIFO, FIFO</h1>
<hr>
<img src="https://tinyurl.com/bderx4bh" width=50% >
<h3> The Monty Language </h3>

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

<h3> Monty byte code files </h3>

Files containing Monty byte codes usually have the .m extension. Most of the industry uses this standard but it is not required by the specification of the language. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument:

<div style="background-color:gray;">
<p>
julien@ubuntu:~/monty$ cat -e bytecodes/000.m
push 0$
push 1$
push 2$
  push 3$
                   pall    $
push 4$
    push 5    $
      push    6        $
pall$
</p>
</div>
Monty byte code files can contain blank lines (empty or made of spaces only, and any additional text after the opcode or its required argument is not taken into account:

<div style="background-color:gray;">
<p>
julien@ubuntu:~/monty$ cat -e bytecodes/001.m
push 0 Push 0 onto the stack$
push 1 Push 1 onto the stack$
$
push 2$
  push 3$
                   pall    $
$
$
                           $
push 4$
$
    push 5    $
      push    6        $
$
pall This is the end of our program. Monty is awesome!$
julien@ubuntu:~/monty$

</P>
</div>

<hr>
<hr>
<strong>Your code will be compiled this way </strong>
<div style="background-color:gray;">
<p>$ gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty</P>
</div>

<h3>Learnign Objectives</h3>
* What do LIFO and FIFO mean
* What is a stack, and when to use it
* What is a queue, and when to use it
* What are the common implementations of stacks and queues
* What are the most common use cases of stacks and queues
* What is the proper way to use global variables
