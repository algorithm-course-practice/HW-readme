# HW-readme
Инструкции по выполнению домашних заданий

1) Для выполнения домашних заданий следует сделать форк репозитория с заданием. Для этого в правом верхнем угло выбрать соответствующий пункт
   
![изображение](https://github.com/multithreading-course-practice/HW-readme/assets/2510580/7ffe753f-e73a-4e9b-8d30-92d95bb0c957)

2) Оставить параметры по умолчанию и нажать `Create fork`
   
![изображение](https://github.com/multithreading-course-practice/HW-readme/assets/2510580/52c813bc-78aa-471e-9a77-83911ee5452d)

3) Когда форк будет создан, нам потребуется склонировать его на локальную машину. Для этого воспользуемся соответствующим пунктом "Code" для получения ссылки на git репозиторий. Рекомендуется использовать SSH протокол

![screen](https://github.com/multithreading-course-practice/HW-readme/assets/2510580/1f77c9f9-f06a-47be-abcc-98414cfc63b4)

3.1) Если у вас ранее не был добавлен SSH ключ в профиль GitHub, его потребуется добавить по [ссылке](https://github.com/settings/ssh/new )

3.2) Если у вас нет локальной пары SSH ключей, их можно сгенерировать по [инструкции](https://docs.github.com/ru/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

3.3) В терминале потребуется выполнить команду (demo+user@gmail.com заменить на почту вашей учетной записи github):

```bash
$ ssh-keygen -t ed25519 -C "demo+user@gmail.com"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/c/Users/demo/.ssh/id_ed25519):   // здесь подтверждаем имя файла для приватного ключа
Enter passphrase (empty for no passphrase): // здесь устанавливаем пароль для приватного ключа, можно оставить пустым, но это менее безопасно
Enter same passphrase again: // повторяем пароль
Your identification has been saved in /c/Users/demo/.ssh/id_ed25519
Your public key has been saved in /c/Users/demo/.ssh/id_ed25519.pub  // тут указывается путь до публичного ключа
The key fingerprint is:
SHA256:pQeBfcQbCl83H2BToxEiQgpr7TYUzzWRSFWKpX3FQpY demo+user@gmail.com
The key's randomart image is:
+--[ED25519 256]--+
|  . .o+=OB*oB+o  |
|   + =+Bo*E+++.. |
|  o + =o++o=.o . |
| . o    o=.   .  |
|    +   S .      |
|   . .   .       |
|                 |
|                 |
|                 |
+----[SHA256]-----+

```

3.4) Далее в файле из файла с публичным ключем получаем его содержимое и на [странице добавления SSH ключа](https://github.com/settings/ssh/new ), добавляем его с произвольным названием

![screen_2](https://github.com/multithreading-course-practice/HW-readme/assets/2510580/61232752-c9be-4640-b409-f00b92f94cb0)

4) Получив ссылку на SSH репозиторий, теперь с помощью следующей команды делаем клонирование на локальную машину (git@github.com:DemoMT2024/hw1.git - заменить на вашу ссылку)

```bash
$ git clone git@github.com:DemoMT2024/hw1.git
$ cd hw1
```

5) Решение рекомендуется фиксировать в отдельной ветке, например answer:

```bash
$ git checkout -b answer
```

6) После изменения файлов, решение фиксируем коммитом:

```bash
$ git commit -a -m "произовльное название коммита"
```

6.1) Если во время коммита было следующее сообщение:

```bash
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

```

Нужно задать имя и почту для подписи коммитов, по указанным командам следует скорректировать почту и имя во всей системе глобально:

```bash
 git config --global user.email "my@email.com"
 git config --global user.name "Demo User"
```

Или же локально только в данном локальном репозитори (без флага --global):

```bash
 git config user.email "my@email.com"
 git config  user.name "Demo User"
```

7) После фиксации решения, нужно отправить изменение на удаленный репозиторий:

```bash
$ git push --set-upstream origin answer
```

8) После успешной отправки изменений на удаленный репозиторий, следует убедиться, что в интерфейсе GitHub появилась ветка с вашим решением. Можно переключиться в новую ветку и ссылку на эту страницу следует отправить в поле для ввода решения в образовательной платформе

   ![screen_3](https://github.com/multithreading-course-practice/HW-readme/assets/2510580/bdb087d0-3b83-45ce-87ba-8722ebc6260d)


## Время проверки

По рабочим дням раз в два дня буду проверять наличие новых решений. В случае возникновения замечаний требующих исправления будет добавлен комментарий.

По выходным в воскресенье вечером буду проверять

В случае возникновения любых вопросов - пишите в чат 
