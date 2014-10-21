---
layout: post
tags : [halting-problem, analysis, what-it-is-not]
---
{% include JB/setup %}

You would have definitely come across at least one cool CS guy who would have remarked "Hey, that's calling for solving Halting problem". (Full disclosure: I am one those cool CS guys!) But most of the time, that statement is irrelevant, if you understand the full implications of what it means by Halting Problem is not computable/decidable.

What Halting problem asserts is, "Given any program P, you can not decide effectively if it will terminate or not". The catch here is any. That's there can't be a "Single Program" which can decide the termination of all possible programs. The thing is, if you happen to find such a Holy Grail, all Mathematicians and Software Engineers will be out of job! :) And, then starts Skynet to destroy the mankind! :P

The reason being, almost all hard "real world" problems can be cast into Halting problem. For instance, if you want to solve the the Fermat's Last theorem without Andrew Wiles awesome genius, you will write a program that tries to find a counter-example to Fermat's Last theorem(which any programming beginner can do) and will ask the "Oracle that computes Halting Problem" if the program will terminate. And Bingo! You solved the riddle that baffled the best minds on this planet for 400 years!

So, what does Halting Problem not mean?
(I really wish, any serious pedagogy is replete with questions of this sort. "How not to do something?"/"What something is not?" gives a lot of insight into what something is, rather than knowing "What it really is?" which is given such an embellished form that the learner feels he's a moron for not being able to come up with that himself and be awe-struck by the elegance of the arguments! :) )

What it does not preclude is, the possibility of a tool/program, which decides the "termination of some programs". That's there can exist tools, which can prove that some programs will terminate or not terminate, for sure.

That's a loop of the form:
``
    {Assume infinite precision arithmetics, and that n is given to be non-negative}
    for (int i = 0; i < n; ++i) {
        sum += i;
    }
    {You know you will come to this place!}
``

is easily decidable to termination. In fact, with a reasonably complex tools, you can prove the termination of algorithms like Insertion sort, Bubble sort etc.

In fact, the whole development of "Static Analysis tools", is to solve "Halting Problem" on some inputs. For instance, one of the common features of Static Analysis tools these days is "Unreachable code detection". Any cool CS guy will tell you that, this is very much equivalent to solving "Halting problem". And rest assured, he's right. The proof is: Given a Halting Problem instance program I, modify it to "I; ExitMessage();" Now you can ask whether "ExitMessage()" is an "Unreachable code". Or to put more concretely, you have a print("Got counterexample") in a program for finding counter-example of "Fermat's Last Theorem", "Is `print` an Unreachable code?" This is certainly hard to solve and a static analyzer won't be able to tell you whether "print" is unreachable or not. But what it can tell you is that:

``
int i = 1;
if (i == 0) {print("Got 0");}
``

It can detect easily that "print is an unreachable code".
That's Static Analysis Tools can detect an Unreachable codes in various complex cases, but not in all cases. The catch here is all. You can keep increasing the awesomeness of your Analysis tool, but no matter how good you get, you will not be able to cover all the "Unreachable code" cases.

So, is it an exercise in futile? Nope, definitely not! Increasing the number of cases on which "Unreachable code detection" works well, is really awesome, as it can unearth a lot of bugs in real-world code, just that such a tool can't solve Fermat's Last Theorem by itself. But who cares! As long as, such a tool detects that an ATM's logic which has a huge amount of code when "money < 0", is actually unreachable, if it can be proved from their code that "money will never be less than 0"

Now, what does this post not mean?
(Keeping in spirit with what i want, in a sane pedagogy)

The idea of giving "Fermat's Last Theorem" is purely for illustration. And any analysis tool, which "understands" Fermat's Last Theorem can indeed decide the "Non-Termination of the Counter-example Search for Fermat's Last Theorem". This is a theoretical possibility, because, We now have a proof of Fermat's Last theorem and an analysis tool can, in theory, have the proof included in it, or at least have it as an "axiom" and have checks which specifically checks for "whether a program is trying to find a counter-example for Fermat's last theorem" (which is not hard to do.) But such an analysis tool won't decide, may be, whether a program that tries to find "counter-example for Goldbach's conjecture" will terminate!
That's there's a limit to what any Advanced Tool can tell you! No matter how awesome a Tool is, there will always be a class of Programs whose termination will never be decidable by it!

So, with this post, am I gonna stop being that "cool CS guy", who wouldn't shout "you are trying to solve Halting Problem", given that all we are upto is to solve it for a partial input instance? Nope, really not! :) I love to flaunt what I know, like my fellow geeks. So, i will definitely shout! But there will be a tinge of guilt at the back of my brain. After all, it knows what am saying is plain bullshit, but such a guilt is not hard to circumvent! ;) And the whole purpose of this post is to incept the same tinge of guilt in my fellow geeks whenever they make that remark! :)
