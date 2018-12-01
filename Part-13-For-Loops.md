# Part 13: For Loops

## Creating For Loops

Let's create a new file in our text editor (mine is named "scala_for_loops.scala"). We'll create a new list called "badgers". 

```
var badgers = List("mushroom", "mushroom", "it's a snake")
```
Now, we'll create a "for loop" using this list. 

*input*

```
for(item <- badgers){
    println("BADGER!")
}
```

As in the last section, mark sure to launch your spark-shell in your text editor. Run your file. 

```
:load scala_for_loops.scala
```

And now we get our badgers!

*output*

```
BADGER!
BADGER!
BADGER!
```
We can also print each individual item in the list. 

*input*

```
for(item <- animals){
    println(item)
}
```

*output*

```
mushroom
mushroom
it's a snake
```
## Looping Through a Range

Next, let's use a "for loop" to loop through a range. We'll use the "Array.range(start, stop, step)" format to create a range from 0 to 20. In Scala (as in other programming languages), remember that this range will go up to but not include 20. We can also use a step argument; I'll use 5 as our step, so we'll return every 5th number. 

*input*

```
for(number <- Array.range(0,20,5)){
    println(number)
}
```

*output*

```
0
5
10
15
```

## If Statement Embedded Within For Loop

Let's create an if-else statement embedded within a for loop. We create a range of 0 to 10 and print whether the number is odd or even. 

*input*

```
for(num <- Range(0,10)){
    if(num%2 == 0){
        println(s"$num is even")
    }else{
        println(s"$num is odd")
    }
}
```

*output*

```
0 is even
1 is odd
2 is even
3 is odd
4 is even
5 is odd
6 is even
7 is odd
8 is even
9 is odd
```

Finally, let's revive our animals list. 

```
var animals = List("aardvark", "hedgehog", "walrus")
```

*input*

```
for(word <- animals){
    if(word.startsWith("a")){
        println(s"$word starts with a a")
    }
}
```

*output*

```
aardvark starts with a a
```