Question:
1. State whether each of the following is true or false. If false, explain why.
(1) Base-class constructors are not inherited by derived classes.
(2) An is-a relationship is implemented via composition.
(3) A Student class has an is-a relationship with the Faculty and
Course classes.
(4) Private members of a private base class are inaccessible to the
derived class.
(5) A base class’s protected members can be accessed in the base-class
definition, in derived-class definitions and in friends of the base
class and its derived classes.


2. Draw an inheritance hierarchy for students at a university. Use Student as
the base class of the hierarchy, then include classes
UndergraduateStudent and GraduateStudent that derive from
Student. Continue to extend the hierarchy as deep (i.e., as many levels) as
possible. For example, Freshman, Sophomore, Junior and Senior
derive from UndergraduateStudent, and DoctoralStudent and
MasterStudent derive from GraduateStudent. After drawing the
hierarchy, discuss the relationships that exist between the classes. (Note: You
don’t need to write any code for this exercise.)


Answer:
1.
(1)False
Explain：
繼承只要是public的member data 跟member function都會被繼承，但根據以下這篇文章所述(http://twmht.github.io/blog/posts/cc/class.html)
有三個例外，那就是建構子 Constructor 和解構子 destructor、operator=() 成員、friends。
建構子跟解構子兩者之所以不會被繼承是因為當子類別的object被生成或是銷毀時候，父類別的的預設建構子(default constructor)和解構子會被自動調用。

(2)False
Explain：
is-a relationship(中文：是一種關係)代表的是繼承關係，而非組合關係。
has-a relationship(中文：有一個關線)是代表組合
故原本句子敘述是錯誤的。

(3)True
Explain：
Falcty(代表是學院的意思)
原文敘述是說學生與學院跟課程有一種關係(繼承)，應該是對的。

(4)Maybe false
Explain：
基本上是不會繼承到private的成員函式或資料。
但是如果父類別的public function裡面有對private data進行操作，則這樣子類別因為繼承，則可能透過這些function來存取到private data。

(5)True
Explain：
根據小螞蟻 於 繼承12-7頁對於protected成員的論述當中，有提及protected成員只能在以下狀況使用：
該基本類別的本體、
該基本類別的成員和friend中、
該基本類別所衍生出的任何類別成員和friend中。
與原文具的論述一樣，故正確的正確的