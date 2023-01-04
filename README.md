
# Lecture 5
```
                                                     Мундариҷа
```
#  1 Object
#  2 Object Methods
#  3 Destructuring and spread
#  4 this
***
***

# Object
> Объекти JavaScript як навъи маълумоти ғайриоддӣ мебошад, ки имкон медиҳад
шумо барои захира кардани якчанд
маҷмӯаҳои маълумот.
let person = {
    firstName: "John",
    lastName : "Doe",
    id       : 5566,
  };
  console.log(person.id) // 5566
  
  ***
  ***
# Object Methods
> 1 Усули Object.entries() массиви додашударо бармегардонад
хосияти шуморашавандаи худи объекти дорои сатри калидӣ [key,
velue] ҷуфтҳо.
.
2 Усули Object.keys() массиви додашударо бармегардонад
номҳои моликияти шуморашавандаи объект, ки дар такрор
ҳамон тартибе, ки ҳалқаи муқаррарӣ хоҳад буд.
.
3  Усули Object.values() массиви додашударо бармегардонад
арзишҳои моликияти шуморашавандаи объект.
...
let obj = {
    name: 'Muhammad',
    lastname: 'Avgonov'
};
console.log(Object.entries(obj)); //[Array(2), Array(2)]
console.log(Object.keys(obj)); // ['name', 'lastname']
console.log(Object.values(obj)); // ['Muhammad', 'Avgonov']
***
***
# Destructuring and spread – Destructuring
> Синтаксиси таъиноти вайронкунанда ифодаи JavaScript мебошад, ки онро месозад
кушодани хосиятҳо аз объект ба тағирёбандаҳои алоҳида имконпазир аст.
let person ={
    name: 'Muhammad', //ном
    age: 20,//сину сол
    weight: 67,//вазн
    height: 178 //қад
};
let {name,age,weight,height} = person;
console.log(name);//Muhammad
console.log(age);//20
console.log(weight);//67
console.log(height);//178
****
***
# Destructuring and spread– spread
> Оператори паҳнкунӣ ... истифода мешавад
васеъ ё паҳн кардани он
бо номгуи худ кор мекунад
хосиятҳои объект.
Барои намуна:
let coloredCircle = {
    ...circle,
    color:'red'
};
console.log(coloredCircle)
.
Шумо метавонед паҳнкуниро истифода баред
оператор барои клон кардани худ
хосиятҳои номбаршавандаи а
объект.
Барои намуна:
let circle = {
    radius:10
};
let clonedCircle ={...circle}
console.log(clonedCircle)
***
***