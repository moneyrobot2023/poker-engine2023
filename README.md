poker-engine
============



Покер-движок для хедз-ап Омахи на TheAIGames.com

Эта версия нашего покерного движка была настроена для локального использования, для вашего удобства. Обратите внимание, что этот движок предназначен не только для игры в хедз-ап омаху и может использоваться и в других версиях покера. Вероятно, в будущем мы будем проводить другие соревнования по покеру.

Для компиляции (Windows cmd):

To compile (Windows cmd):
    
    cd [project folder]
    dir /b /s *.java>sources.txt
    md classes
    javac -d classes @sources.txt
    del sources.txt

To compile (Linux):

    cd [project folder]
    mkdir bin/
    javac -sourcepath src/ -d bin/ `find src/ -name '*.java' -regex '^[./A-Za-z0-9]*$'`
    
To run:

    java nl.starapple.backend.RunPoker 2000 [your bot1] [your bot2] 2>err.txt 1>out.txt
    
[your bot1] could be any command for running a bot process. For instance "java main.BotStarter" or "node /home/user/bot/Bot.js"

2000 is the starting stack for both bots.

Errors will be logged to err.txt, output dump will be logged to out.txt.
