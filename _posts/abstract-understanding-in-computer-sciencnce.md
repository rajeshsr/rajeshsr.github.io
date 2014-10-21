---    
layout: post    
tags : [abstract-understanding, computer-science]    
---    
{% include JB/setup %}    
    
Ask a grandma, who is a bit tech savvy about “How will you go to this site: www.google.com”. She will tell you:    
    
1. Goto the “Start” button    
    
2. Click InternetExplorer    
    
3. Go to the “white box” on top.    
    
4. Type “http://www.google.com” there.    
    
Well, she did remarkably well for her education of CS!    
    
Now, this same question has to be asked to an Engineering guy in CS. Here are possible replies:    
    
An average CS guy: Well, go to the browser of your choice on a OS of your choice and type it in your location bar.    
    
A good CS guy: Well, all it requires is a Http Client. You can use any browser you want or probably write a small Http client to fetch the contents. Rendering may be a pain. Oh, yeah, if all you care about is, just fetch the content, you have utilities like “wget”, “curl” etc., so you can save writing the client!    
    
IMHO, both the guys did very good job! And of course the second guy did an awesome job, at least a lot awesome than the grand ma! :)    
    
Now, come this canonical question, “Given a collection of “N” *objects*, sort them.”    
Here are possible replies:    
    
Student 1: Well, you can do:    
``    
// selection sort    
for (int i = 0; i < n; ++i)    
for (int j = i + 1; j < n; ++j) if (arr[i] > arr[j]) swap(arr[i], arr[j]);    
``    
    
Well, this guy has been given a hammer called “C/C++” and I guess he was given this as an exercise program too many times to write it fast!    
    
Student2:      
Well, you can use counting sort and sort in O(n).      
Q: Can you explain?      
Stud2: Well, you can sort *anything* in O(n) with counting sort.      
Q: O(n)? anything?!!      
Stud2: Oh yes! (triumphantly)      
Q: Ok, write the algorithm for that!      
    
Student2 may write the algo or simply stare at “Q”(let “Q” be the guy who asks question!). But am not sure if he would realize that he is using something more than just a comparison based model at that point.      
    
Student3:      
Well, you can do: sort(vec.begin(), vec.end());      
Q: What does that “sort” function do?!      
Stud3: just sort the vector, what else?      
    
Student4:      
You can do merge sort or quick sort    
// Goes on to explain both well. Also remarks about quicksort worst case behavior!    
Q: Cool!    
    
This guy is indeed very good!    
    
A passionate CS guy:      
Well, given that you said it is a collection of objects, i would assume we will be in a comparison based model? In which case we can’t do anything better than O(nLgn). You can use things like quicksort, merge sort, heap sort etc.(Explains the algo.)    
If your “keys” are integers you can do radix sort; if bounded within a range you can do things like counting sort. (Explains the details..)    
BTW, is your full collection of “objects” in-memory? These sorting assume swapping and random access in O(1). External sorting….    
………..    
    
So, this guys has a clear abstract understanding of how sorting algorithms work and the various pre-conditions assumed by Sorting algorithms. Am not saying “Student4″ doesn’t have that. Probably, he has but wouldn’t flaunt it, unlike me! :P    
But the point here is, you should have such “abstract” understanding of Sorting. I don’t care whether you demonstrate it or not unless am interviewing you for a job! :P    
    
The interesting case is, Student1 and Student3. These guys are no better than the “grand ma” discussed earlier! They are just used to using a hammer(C/C++), without understanding the nature of the hammer in the first place!    
Student2 can be even more pathetic, depending on whether he wrote the algorithm for “Counting Sort”.    
    
The CS education that is being imparted should not just keep on giving “hammers” to the people to do things! It should give them ways of making the “hammer” and show how some “hammers” are good in doing what they do. This is the type of understanding/excellence we should be after.    
    
For instance, knowing that in order to fetch the contents of the web site, all you require is a Http Client that speaks Http Protocol, is very important when the problem to solve is fetch 200000 URLs. In this case, even the knowledge of “go to a browser in some OS”, doesn’t help at all! The ability to do a job at hand, is limited by the “abstract” understanding you have of the common solution used to solve a problem. You should know the pre-condition imposed by the solution very well, also have an understanding of how the solution “uses” those pre-conditions to solve the problem! This understanding helps in “innovating” when you come across a situation which hasn’t been trodden before; this isn’t uncommon in various good S/W engineering problems you would solve.    
    
And the interesting part is, real-world problems are more complicated and interesting to make such distinction of deeper understanding among individuals, as in this case of “sorting” or “browsing”! :)    
    
PS: The idea of using a “grand ma”, is just there purely for illustration. I know 40 years down the line, most “grand ma”s will be tech savvy and will be offended to read this post(hope these blog contents survives till then! :P )! :) Sorry! Also, the present “grand ma” who would read this, please don’t get offended! I suck a lot more in various fields where you rock and feel free to add my name, in the blog that you would write regarding it, like, “if you ask rajeshsr about …..”     
    
