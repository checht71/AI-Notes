1. There is no need to go fully object oriented or functional. Use whatever fits best. Just focus on readability and usability.
2. You should use a class for situations which either A. need a ton of data or B. have a lot of behavior which makes sense to be bundled together. You should not combine A and B or your class will be a mess.
3. Be careful with inheritance. Do not use deep hierarchies of classes and sub-classes. Your OOP should be used to make things *simpler*, not more complicated.
4. OOP is used to make things less redundant and more modular. If you have a specific type of object that you're going to create again and again, use a class. If you have a specific multi-step algorithm that you're going to use again and again, use a class.
5. Don't overuse power features.

[Source](https://www.youtube.com/watch?v=-ghD-XjjO2g)