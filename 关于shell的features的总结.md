#关于shell的features的总结：
##Rationale
在shell中输入任何命令时，都是采用的以下格式`Command [Options] Arguments`。

##Conclusion
针对该格式，可以将shell提供的功能总结成如下三类：
###For Arguments
1. WildCard
2. Brace Expression
3. Quotes
4. Escape

###For Whole Command
1. Combination
2. Redirection
3. Pipes

###For Shell
1. Variable
2. Alias
3. History

##便于记忆
为了方便记忆，总结成：QWEB CRP HAV 三行缩略词。