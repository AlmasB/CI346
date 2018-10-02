### CI346 Lab Session 2

1. Download `grammy.jar` and `input.json` from StudentCentral Week 2 attached files.
Place both files in the same directory.

2. Open Cygwin terminal (or other supported), traverse to the directory where
your downloaded files are and run `grammy.jar`.
For example:

```
cd c:/Users/rs344/Downloads
java -jar grammy.jar
```

If you have run this correctly, you should see something like this:

```
Generated output:
Your emotion is happy!
```

3. Open `input.json` in a text editor.
Consider this line:

```
"emotion" : ["happy", "sad", "proud"],
```

It consists of two parts: symbol, then a set of symbols.
Using the **same** formatting, add a new symbol called `name`,
which expands to some arbitrary set of symbols, for example "Adam", "Bob", "Eve".
Note that if you do not follow the formatting, you might encounter syntax errors.
Feel free to add your own examples.
Next, modify

```
"origin" : ["Your emotion is {emotion}!"]
```

so that it uses your newly created `name` symbol in the sentence.
Finally, run `grammy` to see changes.
One possible output is:

```
Adam's emotion is proud!
```

4. Construct more complex examples with multiple symbols.
Create recursive symbols, for example:

```
"name" : ["{firstName} {lastName}"],
```

5. Have a look at [this example](https://github.com/AlmasB/grammy#example-3).
Based on it, or using your own example, create a narrative using `grammy`
for a movie / video game / book.
If you are feeling brave,
check out [symbol modifiers](https://github.com/AlmasB/grammy/blob/master/src/main/kotlin/com/almasb/grammy/EngModifiers.kt#L17).