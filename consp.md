========================================================
2022.09.03 L1-L4
========================================================
пример простейшего класса:

class App {
        piblic static void main (String[] args){
            System.out.println ("Hello, World!");
        }
}

https://checkstyle.sourceforge.io/checks.html

========================================================
2022.09.04 L5-L8
Мат операции

class App {
        Public static void main (String[] args) {
            System.out.println (3+4);
        }
}
System.otu.println (8/2);
System.out.println (3*3*3);

Основные моменты лекции 5 : Операторы, комутативные операции (перемена мест слагаемых сумма неизменяется), композиция операций, приоритет операций, числа с плавающей точкой.

========================================================
H/W L5
========================================================
Напишите программу, которая считает и последовательно выводит на экран значения следующих математических выражений:
-8 разделить на -4
остаток от деления 100 на 3
сумму двух предыдущих операций

class App {
    public static void printResult(String[] args) {
        // BEGIN (write your solution here)
        System.out.println((-8)/(-4));
        System.out.println(100%3);
        System.out.println(((-8)/(-4))+(100%3));
        // END
    }
}

========================================================
l6
Кавычки, Экранирующие последовательности, конкатенация

символ экранирования \
перенос коретки \n (line feed) в Windows \r\n

Конкатенация строк через +

========================================================
l7 
Переменные, Изменение переменной, Ошибки при работе с переменными, выражения в опредлениях, переменные и конкатенация, константы

объявление переменной - var greeting = "Father!";
Имена переменных регистрозависимы, нельзя начинать с цифры
Для удобства переменные принято создавать наиболее близко к месту использования.
Java статически типизированный язык - тип переменной задается при определении и больше не меняется.
ТИПОВЫЕ ОШИБКИ
переменная должна быть определена до ее исопльзования., объявление уже объявленной переменной.
ВЫРАЖЕНИЯ В ОПРЕДЛЕНИЯХ
КОНСТАНТЫ 
final var PI = 3.14; - Константы принято именовать в ВЕРХНЕМ_РЕГИСТРЕ
========================================================
l8
Именование, Именование переменных, магические числа.

общие правила - не использовать транслит (только английский).
В именовании 3 основных подхода, которые комбинируют друг с другом:
1. kebab-case - составные части переменной разделяются дефисом. прим - my-super-var
2. snake_case - для разделения используется подчеркивание . прим -my_super_var
3. CamelCase - каждое слово в переменной пишется с заглавной буквы. Например MySuperVar
4. lowerCamelCase - каждое слово перменной пишется с заглавной буквы, кроме первого. прим mySyperVar.
В Java используется CamelCase и его вариация lowerCamelCase.

========================================================
2022.09.05 L9-11

Типы данных, Явная типизация, какие бывают типы, значение по умолчанию, значение null, явное преобразование типов

глобально типы в Java делятся на две большие группы:

\\\Примитивные. Предопределены в Java. имена примитивных типов начинаются с нижнего регистра (int).
Примитивные данные всегда имеют значение, даже если они определяются без инициализации.
byte (Байт -128..127), short (2 байта), int ( 4 байта), long (8 байт) ЦЕЛЫЕ ЧИСЛА
float, double, РАЦИОАНЛЬНЫЕ ЧИЛСА
boolean, char

Самые частые типы - int, double, boolean

char ch ='a'; - определятеся через одинарные кавычки. Извлечение символва из строки "hexlet".charAt(1); // e

\\\Ссылочные (не примитивные). Создаются самим программистом (кроме String и Array) имена ссылочных с верхнего (Sting)
значение null. используется для ссылочных типов, когда значение не определено.

\\преобразование типов:
var number = Integer.parseInt ("345");
var result = (int) 5.1 ;
Преобразование можно использовать внутри составных выражений.
var result = 10 + ((int) 5.1);

========================================================
l10
Вызов методов, параметры методов, несколько параметров, значения по умолчанию
методы - это действия, которые нужно выполнить над данными, к которым они применяются.
Объекты - данные у которые есть методы. В Java все не примитивные (ссылочные) типы данных - это объекты.
.lenght(); .toUpperCase();
в вызов метода можно передавать параметры.  .charAt(0); параметров может быть больше одного .replace("go", "mo"); 
Параметры могут содержать значение по умолчанию .substring(1)- извлечть подстроку со 2 символа. .substring(1,3) со второго до 4.

========================================================
l11
Строки в java неизменяемы. любой метод строки может только вернуть новую строку.
var language = "JAVA";
language = language.toLowerCase();
System.out.println(language); // => "java"


========================================================
2022.09.06 l12-

Цепочки вызовов методов

.trim() - обрезка концевых пробелов
.replace(,) - замена символов

name = name.trim()
        .replace("?", "")       
        .replace(" ", "-")
        .toLowerCase();

========================================================
l13
детерменированность, Побочные эффекты
Метод является детерминированным тогда, когдя для одних и тех же входных параметров он возвращает один и тот же результат.
Math.random(); - не детерминированный 

========================================================
l14
Стандартная библиотека.

Основные советы как узнавать о новых методах:
- Всегда четко отслеживать с чем вы сейчас работаетей (какой тип данных). Почти всегда вы найдете необходимый метод в соотвествущем разделе документации - например, для работы со строками нужно изучать строковые методы.
- Периодически открывайте раздел со стандартными методами по изучаемой тематике и просто пробегайтесь по ним, изучая сигнатуры и способы использования.
- Чаще читайте чужой код, особенно код библиотек, которые вы используете. Он весь доступен на GitHub/
Доп. Лекция "Как искать техническую информацию " https://guides.hexlet.io/ru/how-to-search/?roistat_visit=3679276&_gl=1*loplxo*_ga*MTYxMDA5NDE3Ny4xNjQ0NjE0NzM2*_ga_PM3R85EKHN*MTY2MjQ4NjM2NC4xOTguMS4xNjYyNDg2ODAyLjAuMC4w

Варианты документации:
Getting started - куда жать чтобы было весело
Guides - описание отдельных компонентов инструмента
API - сухая документация по всем возможным функциям приложения
Tutorials - вариции исопльзования инструмента.

import java.time.LocalDate;
import java.time.Month;
import java.time.temporal.ChronoUnit;

public class App {
    public static void main(String[] args) {
        // BEGIN (write your solution here)
        LocalDate dateFrom = LocalDate.of(2017, Month.MAY,24);
        LocalDate dateTo = LocalDate.of(2017, Month.JULY,29);
        long noOfDaysBetween = ChronoUnit.DAYS.between(dateFrom,dateTo);
        System.out.println(noOfDaysBetween);
        // END
    }
}

========================================================
l15
Какие бывают методы, вызовы методов у объектов, Вызовы статических методов. Объекты для простоты можно воспринимать как данные, которые доступны внутри метода.
\\вызов метода у объекта:
объект.метод();
user.getName();  currentdate.getDayOfMonth(); file.exists();
System.out.println() - это метод объекта out, который, в свою очередь лежит внутри класса System.
\\статические методы:
вызываются когда действие есть, а объекта нет. (математические операции над числами ил икакие-то действия, которые не относятся к конкретному объекту, а имеют отношение ко всем объектам данного типа.) Опирается на данные которые приходят в виде параметров.
Math.random(); //Получение случайного чилса. Вызов напрямую из класса Math
Files.readString(path); //чтение данных по указанному пути.
НЕЛЬЗЯ ОПРЕДЕЛЯТЬ МЕТОДЫ ВНЕ КЛАССОВ.

Files.readString(path); // Без объекта, статический метод
path.read(); // можно и через объект файла.

СТАТИЧЕСКИЕ МЕТОДЫ ВЫЗЫВАЮТСЯ ИЗ КЛАССА НАПРЯМУЮ.
НЕСТАТИЧЕСКИЕ (методы объектов) ВЫЗЫВАЮТСЯ У КОНКРЕТНЫХ ОБЪЕКТОВ И СТРОЯТ СВОЮ ЛОГИКУ ОТНОСИТЕЛЬНО ДАННЫХ САМОГО ОБЪЕКТА.

========================================================
l16
Определение методов
Пример метода. Задача вывести на экран текущую дату

import java.time.LocalDate;

//Определение метода

public class App {
        Public static void showCurrentDate() {
            //Встроенный метод в Java для получения текущего времени и даты
            var currentDate = LocalDate.now();
            var text = "Today is: " +currentDate;
            System.out.println(text);
        }
}

//вызов метода, обязательно указывать имя класса
App.showCurrentDate();

========================================================
2022.09.07 L17- 
Метод Main

базовая обертка метода
public class App {
    public static void main (String[] args) {
        System.out.println("лорем ипсум");
    }
}

Метод main автоматические вызывается при запуске программы из консоли.

# В файле App находится класс с именем App
java App.java # компилирует и запускает на исполнение
# Внутри запустится метод App.main, если он определён

Общепринятое правило - в одном файле размещается один класс.
Любые статические методы вызываются черзе точку после имени класса, а сами вызовы происходят внутри других методов. БЕЗ ИСКЛЮЧЕНИЙ

public class App {
    
    public static void main(String[] args) {
        App.gogo();
    }
    
    public static void gogo() {
        System.out.println("It works!");
    }
}

========================================================
l18 возврат значений.
Для того чтобы метод мог возвращать значения необходимо 2 вещи
1. Описать тип возвращаемых данных.
2. Выполнить возврат return

Пример:
class App {
    public static String greeting() {
        return "Winter is coming!";
    }
}

return возвращает не только конкретное значение(возможно вернуть почти все что угодно)

public class App {
    // BEGIN (write your solution here)
    public static String sayHurrayThreeTimes() {
        return "hurray! hurray! hurray!";
    }
    // END
}

Вариант преподавателя -   через суммирование переменной.  
// BEGIN
    public static String sayHurrayThreeTimes() {
        var word = "hurray!";
        return word + " " + word + " " + word;
    }
    // END

========================================================
l19 Параметры методов

// Принимает на вход один параметр любого типа
System.out.println("я параметр");
// Принимает на вход индекс, по которому извлекается символ
"какой-то текст".charAt(3); // 'о'
// Принимает на вход два строковых параметра
// первый - что ищем, второй - на что меняем
"google".replace("go", "mo"); // "moogle"
// Принимает на вход два числовых параметра
// первый - начальный индекс (включая), второй - конечный индекс (не включая)
"hexlet".substring(1, 3); // "ex"

задача - реализовать статический метод App.getLastChar() - возвращающий последний символ в строке, переданной ему на вход как парамтер.
Выводы из описания:
1. Нжуно определить статический метод getLastChar() в классе App
2. Метод должен принимать на вход один параметр типа String
3. Метод должен возвращать значение типа char

Определение метода
public static String getLastChar(String str) {
    return str.charAt (str.length()-1);
}

Параметры, при их наличии всегда обязательны.
количество параметров не ограничено, перечисляются через запятую.

========================================================
l20 Необязательные параметры методов

Для описания нескольких вариаций вызова функции используется перегрузка метода
При вызове, во время компиляции выбирается та версия метода, которая совпадает по типу и количеству параметров, если такой метод не будет найдет - вернется ошибка.
class App {
    public static int sum (int x, int y){
        return x + y;
    }
    public static int sum (int x) {
        return x + 10;
    }
}

Для избегания дублирования кода достаточно определить сначала общий метод, который принимает больше всего параметров, а затем вызывать его из тех методов, где есть значения по умолчанию.

class App {
    public static int sum (int x, int y) {
        return x + y;
    }

    public static int sum(int x) {
        return App.sum(x,10);
    }
}

public class App {
    // BEGIN (write your solution here)
    public static String getHiddenCard(String cardnum, int starnum){
        return "*".repeat(starnum)+cardnum.substring(12);
    }
    public static String getHiddenCard(String cardnum) {
        return App.getHiddenCard(cardnum,4);
    }
    // END
}


========================================================
L21 Логические операции
Логический тип,Сравнение строк, Сравнение по ссылке и по значению, Особенности строк, комбинирование операций и методов

Список операций сравнения в Java:

< меньше
<= меньше или равно
> больше
>= больше или равно
== равно
!= не равно

public static boolean isInfant (int age) {
    return age < 1;
}

!одинаковые строки хранятся в одной области памяти (для оптимизации), если одинаковые строки возвращаются методом - они находятся в разных областях памяти.
Для сравннеия строк по значению используется equals():

var name1 = "java".toUpperCase(); // "JAVA"
var name2 = "java".toUpperCase(); // "JAVA"
name1.equals(name2); // true

Так же, в строки встроен метод equalIsIgnoreCase() - выполняет рповерку по значению без учета регистра:
var name1 = "java".toUpperCase(); //"JAVA"
var name2 = "java".toLowerCase(); //"java"
name1.equalsIgnoreCase(name2); //true

Комбинирование операций и методов.

метод для проверки честности:

public static boolean isEven (int number){
    return (number%2) == 0;
}

App.isEven(10); // true
App.isEven(3);// false

Метод проверки заглавной буквы. Алгоритм:
1. Получим и запишем в переменную первый символ из строки-аргумента
2. Сравним, равен ли символ своей большой (заглавной) версии
3. Вернем результат

public static boolean isFirstLetterInUpperCase (String string) {
    var firstLetter = string.charAt(0);
    // Класс Character содержит различные методы для работы с символом
    // Метод isUpperCase() проверяет, что переданный символ в верхнем регистре
    retunr Character.isUpperCase(firstLetter);
}

App.isFirstLetterInUpperCase("marmont"); // false
App.isFirstLetterInUpperCase("Robb"); // true

str1.equals(str2)

проверка на полиндром 
    // BEGIN
    public static boolean isPalindrome(String word) {
        var reversedWord = StringUtils.reverse(word);
        return word.equalsIgnoreCase(reversedWord);
    }
    // END


========================================================
L22 Логические операторы
Пример составного условия (метод проверки пароля)
public static boolean isCOrrectPassword (String password) {
    var length = password.length();
    return length >= 8 && length <= 20;
}

isCorrectPassword("qwerty"); // false
isCorrectPassword("qwerty1234"); // true

&& и (конъюнкция)
|| или (дизъюнкция)
! не (отрицание)

a && b || c; // Без скобок сложно понять приоритет
a && (b || c) // Приоритет очевиден

public static boolean isEven(int number) {
    return number % 2 == 0;
}

isEven(10);  // true
!isEven(10); // false

public class App {
    // BEGIN (write your solution here)
    public static boolean isLeapYear(int inptYear) {
        return (inptYear % 400) ==0 || 
                ((inptYear % 4 ==0) 
                    && (inptYear%100 !=0 ));
    }
    /*
    Альтернативные варианты - вывести в отдельный метод провекру четности, проверку кратности для произвольного числа. */
    // END
}

========================================================
L23 Условные конструкции

Конструкция if, if-else, else if, тернарный оператор

if (sentence.endsWith("?")) {
    return "question";
}

if (x > 5) {
    // Если условие true
} else {
    // Если условие false
}

if (/* что-то */) {

} else if (/* другая проверка */) {

} else if (/* другая проверка */) {

} else {

}

Пример метода определяющего тип предложения

public static String getTypeOfSentece(String sentence) {
    var sentenceType = "";

    if (sentence.endsWith("?")) {
        sentenceType + "question";
    } else if (sentence.endsWith("!")) {
        sentenceType = "exclamation";
    } else {
        sentenceType = "general";
    }
    
    retunr "Sentence is " + sentenceType;
}

тернарный операторв

public static int abs(int number) {
    return number >= 0 ? number : -number;
}

общий шаблон <predicate> ? <expression on true> : <expression on false>

import org.apache.commons.lang3.StringUtils;

public class App {
    // BEGIN (write your solution here)
    public static String convertString(String inptString) {
        if (inptString.equals("")) {
            return "";
        } 
        String firstChar=inptString.substring(0,1);
        if (firstChar.equals(
            firstChar.toLowerCase() 
            )) {
                return StringUtils.reverse(inptString);
        } else return inptString;
    }
    // END
}

более элегантно от преподавателя
Применяется тернарный оператор и класс Character, мето isUpperCase().

public static String convertString(String str) {
    if (str.equals("")) {
        return "";
    }
    
    return Character.isUpperCase(str.charAt(0)) ? str : StringUtils.reverse (str);
}

========================================================
2022.09.08 L24-
L24 Конструкция Switch

switch (status) {
    case "processing":
        // Делаем раз
        break;
    case "paid":
        // Делаем два
        break;
    case "new":
        // Делаем три
        break;
    default: // else
        // Делаем четыре
}

Иногда результат полученный внутри case - это конец выполнения етода, содержащего switch.
В таком случае его нужно как-то вернуть наружу. Для решения этой задачи есть два способа.
Первый способ - можно создать переменную перед switch, заполнить ее в case и затем вернуть значение этой переменной наружу:

class App {
    public static String getExplanation (int count) {
        // объявляем переменную
        String result; 

        //Заполняем
        switch (count) {
            case 1:
                result = "one";
                break;
            case 2:
                result = "two";
                break;
            default:
                result = null;
        }

        // Возвращаем
        return result;
    }
}

Альтернативный способ для данного случая - использование return, поскольку после него никакой код не выполняется, то break не нужен

class App {
    public static String getExplanation (int count) {

        switch (count) {
            case 1:
                return "one";
            case 2:
                return "two";
            default:
                return null;
        }
    }
}

Код со switch длиннее else\if но читать его гораздо проще.
Польза конструкции в том, что она лучше выражает намерение программиста, когда нужно проверять конкретные значения переменной.


public class App {
    // BEGIN (write your solution here)
    public static String getNumberExplanation(int inptNumber){
        switch (inptNumber) {
            case 666:
                return "devil number";
            case 42:
                return "answer for everything";
            case 7:
                return "prime number";
            default: 
                return null;
        }
    }
    // END
}

========================================================
L25 Цикл while

Пример простого метода печати числе до указанного

public static void printNumbers (int lastNumber) {
    var i=1;

    while (i <= lastNumber ) {
        System.out.println(i);
        i = i + 1;
    }
    System.out.println("finished!");
}

App.printNumbers(3);

Синтаксический сахар

a = a + 1 → a += 1
a = a - 1 → a -= 1
a = a * 2 → a *= 2
a = a / 1 → a /= 1
a = a + "foo" → a += "foo"

========================================================
L26 Цикл

Использование циклов, Агрегация данных (строки),Обход строк, Формирование строк в циклах

базовый пример - итератор + сумматор

public static int sumNumbersFromRange(int start, int finish ) {
    var i = start;
    var sum = 0;

    while (i<= finish) {
        sum=sum + i;
        i = i +1;
    }

    return sum;
}

Агрегация данных  (строки)
public static String repeat (String text, int times) {

    var result = "" ;
    var i = 1;

    while (i <= times) {
        result = result + text;
        i = i + 1;
    }

    return result;
}

Метод распечатки слова посимвольно:

public static void printNameBySymbol (String name) {
    var i = 0;

    while ( i < name.length() ) {
        System.out.println(name.charAt(i));
        i += 1;
    }
}

Метод ревесра строки:

public static String reverse (String str) {
    var i = 0;

    var result = "";
    while (i < str.length()) {
        result=str.charAt(i)+ result;
        i += 1;
    }
    return result;
}

public class App {
    public static String joinNumbersFromRange(int start, int finish) {
        // BEGIN (write your solution here)
        var i=start;
        var result="";
        
        while (i <= finish) {
            result += i;
            i+=1;
        }
        
        return result;
        // END
    
    }
}


========================================================
L26 Условия внутри цикла и возврат значений

Метод считате сколько раз входит буква в предложение

public static int countChars (String str, char ch) {
    var i = 0;
    var count = 0;

    while (i < str.length()) {
        if (str.charAt(i) == ch) {
            count += 1;
        }
        i+=1;
    }
    return count;
}

Возврат из циклов
Работа с циклами обычно сводится к вдум сценариям:
1. Агрегация. Накопление результата во время интераций и работ с ним после цикла.
2. Выполнение цикла до достижения необходимого результата и выход.

Метод проверки на простое число

public static boolean isPrime (int number) {
    if (number < 2) {
        return false;
    }

    var divider = 2;

    while (divider <= number/2) {
        if (number % divider == 0) {
            return false;
        }

        divider += 1;
    }

    return true;
}

ДЗ
public class App {
    public static int countChars(String str, char ch) {
        // BEGIN (write your solution here)
        var i = 0;
        var count = 0;
        var chek = Character.toLowerCase(ch);
        var lowStr = str.toLowerCase();

        while (i< str.length()) {
            if (lowStr.charAt(i) == chek) {
                count += 1;
            }

            i +=1;
        }

        return count;
        // END
    }
}