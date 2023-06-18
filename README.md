poker-engine
============



Покер-движок poker-engine.com
----
![poker-engine](https://github.com/moneyrobot2023/poker-engine2023/blob/master/poker.jpg )

Эта версия нашего покерного движка была настроена для локального использования, для вашего удобства. Обратите внимание, что этот движок предназначен не только для игры в хедз-ап омаху и может использоваться и в других версиях покера. Вероятно, в будущем мы будем проводить другие соревнования по покеру.

Для компиляции (Windows cmd):
----
Для компиляции (Windows cmd):
----
cd [project folder]
dir /b /s *.java>sources.txt
md classes
javac -d classes @sources.txt
del sources.txt
----
Для компиляции (Linux):
----
cd [project folder]
----
mkdir bin/
javac -sourcepath src/ -d bin/ `find src/ -name '*.java' -regex '^[./A-Za-z0-9]*$'`
Для запуска:
----

java nl.starapple.backend.RunPoker 2000 [your bot1] [your bot2] 2>err.txt 1>out.txt
[ваш bot1] может быть любой командой для запуска процесса бота. Например, "java main.BotStarter" или "node /home/user/bot/Bot.js"

2000 - это стартовый стек для обоих ботов.
----
Ошибки будут регистрироваться в err.txt , выходной дамп будет регистрироваться в out.txt.
