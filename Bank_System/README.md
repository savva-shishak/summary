## Не большое отступление
Я изучаю язык программирования Java по книге Шилдта "Java8 полное руководство", и все полученные знания пытаюсь применить в этом проекте. Я не говорю о том что вся банковская система выглядит так, просто на её примере пытаюсь показать что я умею. На момент написания этого файла я изучаю наследования в ООП.

Также у меня есть опыт разработки веб-приложений на JavaScript, и если у вас установлен Node.js и NPM, то вы сможени увидет и их

## Описание работы
Я ещё не изучи Java FX для создания графической оболочки и Java EE для того чтобы представить проект в виде дектопного или веб-приложения. Но всё работает в виде консольно приложения.

В Bank_System я написал банковскую логику, о которой сейчас пойдёт речь.

### Bank
Сама логика начинается с объекта Bank или класса Bank.class, объект Bank хранит в себе переменные названия банка, массив объктов Client, о котором я расскажу далее, и счётчик. В будующем я хочу поменять массив и счётчикна базу данных SQL с СУБД PostgreSQL или MySQL. Ещё определён конструктор, в котором инициализируется количество яйчеек в массиве и название банка.

### Client
Класс Client хранит в себе номер карты как id, баланс, статус блокировки (заблокирован или нет), пароль, пароль наоборот (слышал что это необходимо, если человека заставляют снять с карты). кодовое слово, счётчик для того, чтобы считать количество неправильно отправленных паролей на этот счёт, и ссылка на объект User к которому привязан Client. Так же определён конструктор, через который все эти поля инициализируются.

### User
У объекта User есть поля для хранения имени и фамилии пользователя, а также статистическая переменная cout для хранения количества пользователей, через которое инициализируется переменная passport, представляющая из себя просто порядковый номер пользователя.

### Status
Status - это перечисление. Хранит в себе статусы перевода, списания, зачисления денег и т.д.

## Проект
В классе Bank определены методы для снятия со счёта, зачисления на счёт и переврда денег между счетами. Позже я хочу изучить Java EE и связать эти классы с веб-приложением и базой данных, и фронтальную часть сделать на JS. В файле Program.java показано как работает программа. Запустить её и посмотреть результат можно в терминале или командной строке через:
"""
javac Bank_System/Program.java && java Bank_System.Program.
"""
