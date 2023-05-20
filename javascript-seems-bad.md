Javascript will let me compare variables of different types. Why would we compare apples and oranges :(  
![Screenshot from 2023-05-17 18-08-45](https://github.com/Massinja/learning-progress/assets/84927906/d791fffb-c127-4c38-8202-ac121064c3a7)

Javascript will let me reassign a value within an "if statement". That is completely broken.
![Screenshot from 2023-05-17 18-11-05](https://github.com/Massinja/learning-progress/assets/84927906/7f11689c-d899-4e6e-ac3b-d61e5d95569b)
![Screenshot from 2023-05-17 18-12-16](https://github.com/Massinja/learning-progress/assets/84927906/f9613d5a-7cc9-44f5-be43-45ec0f9fe66b)

Scope of the variable should end at the end of the innermost containing block, but not in JS :( again such an assignment within the if statement should not be even allowed  
![Screenshot from 2023-05-17 18-14-05](https://github.com/Massinja/learning-progress/assets/84927906/9606e808-641a-42df-8e2a-03aa6dfbfb43)

At first glance, it seems that array starts to act as a hash table, however, it  doesn't consider those key-value pairs in its length.
It turns out, all the random index values, including negative integers become a property of an Array Object. You can access them through the dot notation, but not the negative integer. Also treats -1 and "-1" as the same property

    const list = [0, 1, 3, 5, 6]
    console.log(list)
    list[-1] = 76
    list["random"] = 98
    let len = list.length
    console.log(list)
    console.log("length of the list is", len)

    list["-1"] = 108    // will reassign list[-1]
    console.log(list[-1])

    console.log(list.random)
    //console.log(list.-1) // SyntaxError! but wasn't "-1" object's property?
    



