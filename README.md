[![N|Solid](featured.jpg)
```
                                                          Information
```
***
***
##### Дар JavaScript сана ва вақт бо объекти Date муаррифӣ мешавад. Объекти Date
##### маълумоти сана ва вақтро пешниҳод мекунад ва инчунин усулҳои гуногунро пешниҳод мекунад.
##### Санаи JavaScript давраи EcmaScript-ро муайян мекунад, ки миллисонияҳоро ифода мекунад
##### аз 1 январи соли 1970 UTC. Ин сана ва вақт ба давраи UNIX баробар аст
##### (арзиши бартаридоштаи асосӣ барои арзишҳои сана ва вақт аз ҷониби компютер сабтшуда)
***
***
```
                                                        Creating Date Objects
```
>Санаи объектҳо бо new Date()созанда сохта мешаванд.
9 роҳи эҷоди объекти нави сана вуҷуд дорад :
..
 new Date()
new Date(date string)
new Date(year,month)
new Date(year,month,day)
new Date(year,month,day,hours)
new Date(year,month,day,hours,minutes)
new Date(year,month,day,hours,minutes,seconds)
new Date(year,month,day,hours,minutes,seconds,ms)
new Date(milliseconds)
...

***
***
>new Date()
const add = new Date();
console.log(add) //Thu Jan 05 2023 21:01:55 GMT+0500 (Tajikistan Time)
***
>new Date(date string)
const add = new Date("01-02-2001")
console.log(add) //Tue Jan 02 2001 00:00:00 GMT+0500 (Tajikistan Time)
***
>new Date(year,month)
const add = new Date(2001,01)
console.log(add) // Thu Feb 01 2001 00:00:00 GMT+0500 (Tajikistan Time)
***
...
***
>new Date(year,month,day,hours,minutes,seconds,ms)
const add = new Date(2001,01,15,21,45,59)
console.log(add) // Thu Feb 15 2001 21:45:59 GMT+0500 (Tajikistan Time)
***
```
  Method                                     	Description

getFullYear()                    	Get year as a four digit number (yyyy)
getMonth()	                        Get month as a number (0-11)
getDate()	                        Get day as a number (1-31)
getDay()	                        Get weekday as a number (0-6)
getHours()                      	Get hour (0-23)
getMinutes()	                    Get minute (0-59)
getSeconds()	                    Get second (0-59)
getMilliseconds()	                Get millisecond (0-999)
getTime()	                        Get time (milliseconds since January 1, 1970)
```

#### Усули getFullYear().
>Усул getFullYear()соли санаро ҳамчун рақами чор рақам бармегардонад:
let d = new Date("2021-03-25");
console.log(d.getFullYear()) //2021
****
****
#### Усули getMonth().
>Усул getMonth()моҳи санаро ҳамчун рақам (0-11) бармегардонад.
let months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
let d = new Date("2021-03-25");
let month = months[d.getMonth()];
console.log(month)//March
***
***
#### getDate()	
>Усул getDate()рӯзи санаро ҳамчун рақам бармегардонад (1-31):
let d = new Date("2021-03-25");
console.log(d.getDate()) //25
***
***
#### getHours()  
>Усул getHours()соатҳои санаро ҳамчун рақам бармегардонад (0-23):
let d = new Date(2002,10,18,12,25,45);
console.log(d.getHours()) // 12
***
***
#### Усули getMinutes().
>Усул getMinutes()дақиқаҳои санаро ҳамчун рақам бармегардонад (0-59):
let d = new Date(2002,10,18,12,25,45);
console.log(d.getMinutes()) // 25
***
***
#### getSeconds()	
>Усул getSeconds()сонияҳои санаро ҳамчун рақам бармегардонад (0-59):
let d = new Date(2002,10,18,12,25,45);
console.log(d.getSeconds()) // 45
***
***
#### Усули getMilliseconds().
>Усул getMilliseconds()миллисонияҳои санаро ҳамчун рақам (0-999) бармегардонад:
let d = new Date(2002,10,18,12,25,45,875);
console.log(d.getMilliseconds()) // 875
***
***
#### Усули getTime().
> Усул getTime()шумораи миллисонияҳоро аз 1 январи соли 1970 бармегардонад:
let d = new Date(2002,10,18,12,25,45,875);
console.log(d.getTime()) // 1037604345875
***
***
#### Усули getDay().
>Ин getDay()усул рӯзи ҳафтаи санаро ҳамчун рақам (0-6) бармегардонад.
let d = new Date(1970,01,02,12,25,45,875);
console.log(d.getDay()+1) // 2
***
***
#### Усули Date.now().
>Date.now()микдори милли сонияхоро аз 1 январи соли 1970 бармегардонад.
let ms = Date.now();
console.log(ms)//1672939798903
***
***
***
#### Усули setFullYear
>setFullYear()соли санаро муқаррар мекунад.
setFullYear()инчунин метавонад моҳ ва рӯзро муқаррар кунад.
const d = new Date();
d.setFullYear(2015);
console.log(d) //Mon Jan 05 2015 23:30:24 GMT+0500 (Tajikistan Time)

#### Усули setDate()
>setDate()рӯзи моҳи санаро муқаррар мекунад.
let d = new Date();
d.setDate(15);
console.log(d) //Sun Jan 15 2023 23:36:25 GMT+0500 (Tajikistan Time)

...
***
***


















[![N|Solid](img_2.png)
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
    id       : 0301,
  };
  console.log(person.id) // 0301
  
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

[![N|Solid](img_1.png)


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
# "this" in JavaScript
> "this" ин тағирёбанда нест. Ин калимаи калидӣ аст.
Шумо арзиши онро тағир дода наметавонед.
***
>Дар JavaScript, "this" калимаи калидӣ ба объект ишора мекунад.
Кадом объект аз он вобаста аст, ки "this" чӣ гуна даъват карда мешавад (истифода мешавад ё даъват мешавад).
"this" калимаи калидӣ вобаста ба тарзи истифодааш ба объектҳои гуногун ишора мекунад:
```
Дар усули объект, ин ба объект дахл дорад.
Танҳо ин ба объекти глобалӣ дахл дорад.
Дар функсия, ин ба объекти глобалӣ дахл дорад.
Дар функсия, дар ҳолати қатъӣ, ин номуайян аст.
Дар ҳодиса, ин ба унсуре дахл дорад, ки ҳодисаро қабул кардааст.
Усулҳо ба монанди call(), application() ва bind() метавонанд инро ба ягон объект ишора кунанд.
```
# "this" Афзалият (Precedence)

>Барои муайян кардани он ки
объект, ки ба он ишора мекунад;
Истифодаи зеринро истифода баред
афзалияти тартибот:
1 bind()
2 apply() and call()
3 Object method
4 Global scope

***
Explicit Function Binding(Ҳатмӣ будани функсияи ошкор)
>Усулҳои call() ва application() усулҳои пешакӣ муайяншудаи JavaScript мебошанд.
Ҳардуи онҳоро метавон истифода бурд, ки усули объектро бо объекти дигар ҳамчун далел даъват кунад.

### "this" дар як метод
>Вақте ки дар усули объект истифода мешавад, "this" ба объект дахл дорад.
Дар мисоли болои ин саҳифа, ин ба объекти person  дахл дорад.
Зеро усули fullName усули объекти person  аст:
let person = {
    firstName: "Muhammad",
    lastName : "Ali",
    id       : 0304,
     fullName : function() {
     return this.firstName + " " + this.lastName;
    }
  };
  console.log(person.fullName()) // John Doe
  
  ***
  ***
### this Alone (Танҳо)
> Вақте ки танҳо истифода мешавад, ин ба объекти глобалӣ дахл дорад.
Зеро ин дар миқёси ҷаҳонӣ кор мекунад.
Дар равзанаи браузер объекти глобалӣ [object Window]
let a = this;
console.log(this) //Window{window: Window, self: Window...}
*****
***
### bind()
>Бо усули bind() объект метавонад методро аз объекти дигар қарз гирад.
Ин мисол 2 объектро (шахс ва аъзо) месозад.
Объекти аъзо усули номи пурраро аз объекти шахс мегирад:
let person = {
    firstName: "Ali",
    lastName: "Asadzoda",
    age:20,
    fullName:function(){
        return this.firstName+" "+this.lastName;
    }
};
let member ={
    firstName:"Ahamad",
    lastName:"Anvarzoda"
}
let fullName = person.fullName.bind(member)
console.log(fullName()) //Ahamad Anvarzoda

***
***
### apply() 
>Усул apply()далелҳоро ҳамчун массив мегирад .
Усул apply()аргументҳоро дар массив қабул мекунад:
let numbers = [1,2,3,4,5,6,7,8,9,10]
let sum = Math.max.apply(null,numbers)
let sum2 = Math.min.apply(null,numbers)
console.log(`max= ${sum}   min= ${sum2} `) //max= 10   min= 1 

***
### call()
>Усул call()далелҳоро алоҳида мегирад .
function Product(name,price){
    this.name=name,
    this.price=price;

}
function Food(name,price){
   Product.call(this,name,price);
   this.category = 'food';

}
console.log(new Food('cheese').name)






