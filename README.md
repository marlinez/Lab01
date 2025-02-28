# Lab01
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

marialuneva@1511:~$ export GITHUB_USERNAME=marlinez
marialuneva@1511:~$ export GIST_TOKEN=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
marialuneva@1511:~$ alias edit=nano
marialuneva@1511:~$ mkdir -p ${GITHUB_USERNAME}/workspace
marialuneva@1511:~$ cd ${GITHUB_USERNAME}/workspace
marialuneva@1511:~/marlinez/workspace$ pwd
/home/marialuneva/marlinez/workspace
marialuneva@1511:~/marlinez/workspace$ cd ..
marialuneva@1511:~/marlinez$ pwd
/home/marialuneva/marlinez
marialuneva@1511:~/marlinez$ mkdir -p workspace/tasks/
marialuneva@1511:~/marlinez$ mkdir -p workspace/projects/
marialuneva@1511:~/marlinez$ mkdir -p workspace/reports/
marialuneva@1511:~/marlinez$ cd workspace
marialuneva@1511:~/marlinez/workspace$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2025-02-28 22:18:46--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Распознаётся nodejs.org (nodejs.org)… 104.20.22.46, 104.20.23.46, 2606:4700:10::6814:162e, ...
Подключение к nodejs.org (nodejs.org)|104.20.22.46|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 9356460 (8,9M) [application/x-xz]
Сохранение в: ‘node-v6.11.5-linux-x64.tar.xz’

node-v6.11.5-linux- 100%[===================>]   8,92M  1,17MB/s    за 6,9s    

2025-02-28 22:18:53 (1,29 MB/s) - ‘node-v6.11.5-linux-x64.tar.xz’ сохранён [9356460/9356460]

marialuneva@1511:~/marlinez/workspace$ tar -xf node-v6.11.5-linux-x64.tar.xz
marialuneva@1511:~/marlinez/workspace$ rm -rf node-v6.11.5-linux-x64.tar.xz
marialuneva@1511:~/marlinez/workspace$ mv node-v6.11.5-linux-x64 node
marialuneva@1511:~/marlinez/workspace$ ls node/bin
node  npm
marialuneva@1511:~/marlinez/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin
marialuneva@1511:~/marlinez/workspace$ export PATH=${PATH}:`pwd`/node/bin
marialuneva@1511:~/marlinez/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin:/home/marialuneva/marlinez/workspace/node/bin
marialuneva@1511:~/marlinez/workspace$ mkdir scripts
marialuneva@1511:~/marlinez/workspace$ cat > scripts/activate<<EOF
> export PATH=\${PATH}:`pwd`/node/bin
> EOF
marialuneva@1511:~/marlinez/workspace$ source scripts/activate
marialuneva@1511:~/marlinez/workspace$ gem install gist
Команда «gem» не найдена, но может быть установлена с помощью:
sudo apt install ruby-rubygems
marialuneva@1511:~/marlinez/workspace$ sudo apt install ruby-rubygems
[sudo] пароль для marialuneva: 
Попробуйте ещё раз.
[sudo] пароль для marialuneva: 
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Будут установлены следующие дополнительные пакеты:
  fonts-lato javascript-common libjs-jquery libruby libruby3.2 rake ruby
  ruby-net-telnet ruby-sdbm ruby-webrick ruby-xmlrpc ruby3.2
  rubygems-integration
Предлагаемые пакеты:
  apache2 | lighttpd | httpd ri ruby-dev bundler
Следующие НОВЫЕ пакеты будут установлены:
  fonts-lato javascript-common libjs-jquery libruby libruby3.2 rake ruby
  ruby-net-telnet ruby-rubygems ruby-sdbm ruby-webrick ruby-xmlrpc ruby3.2
  rubygems-integration
Обновлено 0 пакетов, установлено 14 новых пакетов, для удаления отмечено 0 пакетов, и 35 пакетов не обновлено.
Необходимо скачать 8 926 kB архивов.
После данной операции объём занятого дискового пространства возрастёт на 41,1 MB.
Хотите продолжить? [Д/н] yes
Пол:1 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 fonts-lato all 2.015-1 [2 781 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 javascript-common all 11+nmu1 [5 936 B]
Пол:3 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 libjs-jquery all 3.6.1+dfsg+~3.5.14-1 [328 kB]
Пол:4 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 rubygems-integration all 1.18 [5 336 B]
Пол:5 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 ruby3.2 amd64 3.2.3-1ubuntu0.24.04.3 [50,7 kB]
Пол:6 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 ruby-rubygems all 3.4.20-1 [238 kB]
Пол:7 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 ruby amd64 1:3.2~ubuntu1 [3 466 B]
Пол:8 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 rake all 13.0.6-3 [61,6 kB]
Пол:9 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 ruby-net-telnet all 0.2.0-1 [13,3 kB]
Пол:10 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 ruby-webrick all 1.8.1-1ubuntu0.1 [52,6 kB]
Пол:11 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 ruby-xmlrpc all 0.3.2-2 [24,8 kB]
Пол:12 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 ruby-sdbm amd64 1.0.0-5build4 [16,2 kB]
Пол:13 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 libruby3.2 amd64 3.2.3-1ubuntu0.24.04.3 [5 341 kB]
Пол:14 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 libruby amd64 1:3.2~ubuntu1 [4 694 B]
Получено 8 926 kB за 7с (1 200 kB/s)                                           
Выбор ранее не выбранного пакета fonts-lato.
(Чтение базы данных … на данный момент установлено 149404 файла и каталога.)
Подготовка к распаковке …/00-fonts-lato_2.015-1_all.deb …
Распаковывается fonts-lato (2.015-1) …
Выбор ранее не выбранного пакета javascript-common.
Подготовка к распаковке …/01-javascript-common_11+nmu1_all.deb …
Распаковывается javascript-common (11+nmu1) …
Выбор ранее не выбранного пакета libjs-jquery.
Подготовка к распаковке …/02-libjs-jquery_3.6.1+dfsg+~3.5.14-1_all.deb …
Распаковывается libjs-jquery (3.6.1+dfsg+~3.5.14-1) …
Выбор ранее не выбранного пакета rubygems-integration.
Подготовка к распаковке …/03-rubygems-integration_1.18_all.deb …
Распаковывается rubygems-integration (1.18) …
Выбор ранее не выбранного пакета ruby3.2.
Подготовка к распаковке …/04-ruby3.2_3.2.3-1ubuntu0.24.04.3_amd64.deb …
Распаковывается ruby3.2 (3.2.3-1ubuntu0.24.04.3) …
Выбор ранее не выбранного пакета ruby-rubygems.
Подготовка к распаковке …/05-ruby-rubygems_3.4.20-1_all.deb …
Распаковывается ruby-rubygems (3.4.20-1) …
Выбор ранее не выбранного пакета ruby.
Подготовка к распаковке …/06-ruby_1%3a3.2~ubuntu1_amd64.deb …
Распаковывается ruby (1:3.2~ubuntu1) …
Выбор ранее не выбранного пакета rake.
Подготовка к распаковке …/07-rake_13.0.6-3_all.deb …
Распаковывается rake (13.0.6-3) …
Выбор ранее не выбранного пакета ruby-net-telnet.
Подготовка к распаковке …/08-ruby-net-telnet_0.2.0-1_all.deb …
Распаковывается ruby-net-telnet (0.2.0-1) …
Выбор ранее не выбранного пакета ruby-webrick.
Подготовка к распаковке …/09-ruby-webrick_1.8.1-1ubuntu0.1_all.deb …
Распаковывается ruby-webrick (1.8.1-1ubuntu0.1) …
Выбор ранее не выбранного пакета ruby-xmlrpc.
Подготовка к распаковке …/10-ruby-xmlrpc_0.3.2-2_all.deb …
Распаковывается ruby-xmlrpc (0.3.2-2) …
Выбор ранее не выбранного пакета ruby-sdbm:amd64.
Подготовка к распаковке …/11-ruby-sdbm_1.0.0-5build4_amd64.deb …
Распаковывается ruby-sdbm:amd64 (1.0.0-5build4) …
Выбор ранее не выбранного пакета libruby3.2:amd64.
Подготовка к распаковке …/12-libruby3.2_3.2.3-1ubuntu0.24.04.3_amd64.deb …
Распаковывается libruby3.2:amd64 (3.2.3-1ubuntu0.24.04.3) …
Выбор ранее не выбранного пакета libruby:amd64.
Подготовка к распаковке …/13-libruby_1%3a3.2~ubuntu1_amd64.deb …
Распаковывается libruby:amd64 (1:3.2~ubuntu1) …
Настраивается пакет javascript-common (11+nmu1) …
Настраивается пакет fonts-lato (2.015-1) …
Настраивается пакет rubygems-integration (1.18) …
Настраивается пакет ruby-net-telnet (0.2.0-1) …
Настраивается пакет ruby-webrick (1.8.1-1ubuntu0.1) …
Настраивается пакет libjs-jquery (3.6.1+dfsg+~3.5.14-1) …
Настраивается пакет ruby-xmlrpc (0.3.2-2) …
Настраивается пакет ruby3.2 (3.2.3-1ubuntu0.24.04.3) …
Настраивается пакет libruby:amd64 (1:3.2~ubuntu1) …
Настраивается пакет ruby (1:3.2~ubuntu1) …
Настраивается пакет rake (13.0.6-3) …
Настраивается пакет libruby3.2:amd64 (3.2.3-1ubuntu0.24.04.3) …
Настраивается пакет ruby-rubygems (3.4.20-1) …
Настраивается пакет ruby-sdbm:amd64 (1.0.0-5build4) …
Обрабатываются триггеры для fontconfig (2.15.0-1.1ubuntu2) …
Обрабатываются триггеры для libc-bin (2.39-0ubuntu8.4) …
Обрабатываются триггеры для man-db (2.12.0-4build2) …
marialuneva@1511:~/marlinez/workspace$ gem install gist
Fetching gist-6.0.0.gem
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /var/lib/gems/3.2.0 directory.
	/usr/lib/ruby/vendor_ruby/rubygems/installer.rb:713:in `verify_gem_home'
	/usr/lib/ruby/vendor_ruby/rubygems/installer.rb:903:in `pre_install_checks'
	/usr/lib/ruby/vendor_ruby/rubygems/installer.rb:303:in `install'
	/usr/lib/ruby/vendor_ruby/rubygems/resolver/specification.rb:105:in `install'
	/usr/lib/ruby/vendor_ruby/rubygems/request_set.rb:195:in `block in install'
	/usr/lib/ruby/vendor_ruby/rubygems/request_set.rb:183:in `each'
	/usr/lib/ruby/vendor_ruby/rubygems/request_set.rb:183:in `install'
	/usr/lib/ruby/vendor_ruby/rubygems/commands/install_command.rb:215:in `install_gem'
	/usr/lib/ruby/vendor_ruby/rubygems/commands/install_command.rb:231:in `block in install_gems'
	/usr/lib/ruby/vendor_ruby/rubygems/commands/install_command.rb:224:in `each'
	/usr/lib/ruby/vendor_ruby/rubygems/commands/install_command.rb:224:in `install_gems'
	/usr/lib/ruby/vendor_ruby/rubygems/commands/install_command.rb:170:in `execute'
	/usr/lib/ruby/vendor_ruby/rubygems/command.rb:328:in `invoke_with_build_args'
	/usr/lib/ruby/vendor_ruby/rubygems/command_manager.rb:253:in `invoke_command'
	/usr/lib/ruby/vendor_ruby/rubygems/command_manager.rb:193:in `process_args'
	/usr/lib/ruby/vendor_ruby/rubygems/command_manager.rb:151:in `run'
	/usr/lib/ruby/vendor_ruby/rubygems/gem_runner.rb:52:in `run'
	/usr/bin/gem:12:in `<main>'
marialuneva@1511:~/marlinez/workspace$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
marialuneva@1511:~/marlinez/workspace$ export LAB_NUMBER=01
marialuneva@1511:~/marlinez/workspace$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Команда «git» не найдена, но может быть установлена с помощью:
sudo apt install git
marialuneva@1511:~/marlinez/workspace$ sudo apt install git
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Будут установлены следующие дополнительные пакеты:
  git-man liberror-perl
Предлагаемые пакеты:
  git-daemon-run | git-daemon-sysvinit git-doc git-email git-gui gitk gitweb
  git-cvs git-mediawiki git-svn
Следующие НОВЫЕ пакеты будут установлены:
  git git-man liberror-perl
Обновлено 0 пакетов, установлено 3 новых пакетов, для удаления отмечено 0 пакетов, и 35 пакетов не обновлено.
Необходимо скачать 4 804 kB архивов.
После данной операции объём занятого дискового пространства возрастёт на 24,5 MB.
Хотите продолжить? [Д/н] yes
Пол:1 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 liberror-perl all 0.17029-2 [25,6 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 git-man all 1:2.43.0-1ubuntu7.2 [1 100 kB]
Пол:3 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 git amd64 1:2.43.0-1ubuntu7.2 [3 679 kB]
Получено 4 804 kB за 2с (1 925 kB/s) 
Выбор ранее не выбранного пакета liberror-perl.
(Чтение базы данных … на данный момент установлено 152487 файлов и каталогов.)
Подготовка к распаковке …/liberror-perl_0.17029-2_all.deb …
Распаковывается liberror-perl (0.17029-2) …
Выбор ранее не выбранного пакета git-man.
Подготовка к распаковке …/git-man_1%3a2.43.0-1ubuntu7.2_all.deb …
Распаковывается git-man (1:2.43.0-1ubuntu7.2) …
Выбор ранее не выбранного пакета git.
Подготовка к распаковке …/git_1%3a2.43.0-1ubuntu7.2_amd64.deb …
Распаковывается git (1:2.43.0-1ubuntu7.2) …
Настраивается пакет liberror-perl (0.17029-2) …
Настраивается пакет git-man (1:2.43.0-1ubuntu7.2) …
Настраивается пакет git (1:2.43.0-1ubuntu7.2) …
Обрабатываются триггеры для man-db (2.12.0-4build2) …
marialuneva@1511:~/marlinez/workspace$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Клонирование в «tasks/lab01»...
remote: Enumerating objects: 74, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 74 (delta 0), reused 1 (delta 0), pack-reused 71 (from 1)
Получение объектов: 100% (74/74), 945.07 КиБ | 1.87 МиБ/с, готово.
Определение изменений: 100% (20/20), готово.
marialuneva@1511:~/marlinez/workspace$ mkdir reports/lab${LAB_NUMBER}
marialuneva@1511:~/marlinez/workspace$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
marialuneva@1511:~/marlinez/workspace$ cd reports/lab${LAB_NUMBER}
marialuneva@1511:~/marlinez/workspace/reports/lab01$ edit REPORT.md
marialuneva@1511:~/marlinez/workspace/reports/lab01$ gist REPORT.md
Команда «gist» не найдена, но может быть установлена с помощью:
sudo apt install yorick
marialuneva@1511:~/marlinez/workspace/reports/lab01$ sudo apt install yorick
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Будут установлены следующие дополнительные пакеты:
  rlwrap yorick-data yorick-z
Предлагаемые пакеты:
  yorick-full yorick-mpy-openmpi | yorick-mpy-mpich2 emacsen curl
Следующие НОВЫЕ пакеты будут установлены:
  rlwrap yorick yorick-data yorick-z
Обновлено 0 пакетов, установлено 4 новых пакетов, для удаления отмечено 0 пакетов, и 35 пакетов не обновлено.
Необходимо скачать 1 443 kB архивов.
После данной операции объём занятого дискового пространства возрастёт на 4 538 kB.
Хотите продолжить? [Д/н] yes
Пол:1 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 rlwrap amd64 0.46.1-1build2 [107 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 yorick-data all 2.2.04+dfsg1-12build3 [505 kB]
Пол:3 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 yorick amd64 2.2.04+dfsg1-12build3 [795 kB]
Пол:4 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 yorick-z amd64 1.2.0+cvs20080115-5.1build2 [36,7 kB]
Получено 1 443 kB за 1с (1 793 kB/s) 
Выбор ранее не выбранного пакета rlwrap.
(Чтение базы данных … на данный момент установлен 153571 файл и каталог.)
Подготовка к распаковке …/rlwrap_0.46.1-1build2_amd64.deb …
Распаковывается rlwrap (0.46.1-1build2) …
Выбор ранее не выбранного пакета yorick-data.
Подготовка к распаковке …/yorick-data_2.2.04+dfsg1-12build3_all.deb …
Распаковывается yorick-data (2.2.04+dfsg1-12build3) …
Выбор ранее не выбранного пакета yorick.
Подготовка к распаковке …/yorick_2.2.04+dfsg1-12build3_amd64.deb …
Распаковывается yorick (2.2.04+dfsg1-12build3) …
Выбор ранее не выбранного пакета yorick-z.
Подготовка к распаковке …/yorick-z_1.2.0+cvs20080115-5.1build2_amd64.deb …
Распаковывается yorick-z (1.2.0+cvs20080115-5.1build2) …
Настраивается пакет yorick-data (2.2.04+dfsg1-12build3) …
Настраивается пакет rlwrap (0.46.1-1build2) …
update-alternatives: используется /usr/bin/rlwrap для предоставления /usr/bin/readline-editor (readline-editor) в автома
тическом режиме
/usr/share/rlwrap/filters/ftp_filter.py:57: SyntaxWarning: invalid escape sequence '\s'
  results = [re.split('\s+', l)[dir_filename_column[where]] for l in lines]
/usr/share/rlwrap/filters/ftp_filter.py:100: SyntaxWarning: invalid escape sequence '\s'
  nwords = len(re.split('\s+', line))
/usr/share/rlwrap/filters/ftp_filter.py:108: SyntaxWarning: invalid escape sequence '\s'
  command = re.search('\s*(\S+)', line).group(1)
/usr/share/rlwrap/filters/rlwrapfilter.py:4: SyntaxWarning: invalid escape sequence '\s'
  """
/usr/share/rlwrap/filters/rlwrapfilter.py:211: SyntaxWarning: invalid escape sequence '\S'
  m = re.match("(\S+) (.*?)\r?\n", sys.stdin.readline())
Настраивается пакет yorick (2.2.04+dfsg1-12build3) …
Настраивается пакет yorick-z (1.2.0+cvs20080115-5.1build2) …
Обрабатываются триггеры для man-db (2.12.0-4build2) …
Обрабатываются триггеры для install-info (7.1-3build2) …
marialuneva@1511:~/marlinez/workspace/reports/lab01$ gist REPORT.md
gist: (WARNING) fread failed (command) on CGM file REPORT.md
gist: (WARNING) BEGIN METAFILE element missing
gist: (WARNING) REPORT.md is not a binary CGM, cannot open
gist> 
